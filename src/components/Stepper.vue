<script setup lang="ts">
import { ref } from "vue";

// Define los props del componente
const props = defineProps<{ loop?: boolean }>();

// Define los slots del componente
const slots = defineSlots();
const currentStep = ref(0);

// Obtén el contenido del slot predeterminado
const children = slots.default ? slots.default() : [];

const next = () => {
  if (!props.loop) if (currentStep.value >= children.length - 1) return;

  currentStep.value = (currentStep.value + 1) % children.length;
};

const back = () => {
  if (!props.loop) if (currentStep.value <= 0) return;
  currentStep.value =
    (currentStep.value - 1 + children.length) % children.length;
};

// const goTo = (index: number) => {
//   currentStep.value = index;
// };
</script>

<template>
  <div class="relative overflow-x-hidden">
    <div
      class="flex flex-row items-center transition-all ease-out duration-300 overflow-x-hidden"
      :style="{
        width: children.length * 100 + '%',
        transform: `translateX(-${(100 / children.length) * currentStep}%)`,
      }"
    >
      <template v-for="node in children" :key="node.key ?? 'default-key'">
        <div
          :style="{
            width: `calc(100% / ${children.length})`,
          }"
        >
          <component :is="node"></component>
        </div>
      </template>
    </div>
    <button @click="next">Next</button>
    <button @click="back">Back</button>
  </div>
</template>
