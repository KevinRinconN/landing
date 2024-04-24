<script setup lang="ts">
import Header from "../components/Header.vue";
import Stepper from "../components/Stepper.vue";
</script>

<template>
  <Header />
  <section
    class="mx-auto max-w-6xl my-16 text-pretty px-6 text-left text-xl sm:px-20"
  >
    <Stepper class="" loop>
      <div class="grid grid-cols-2 gap-8">
        <div class="flex flex-col justify-center">
          <h1 class="text-2xl">DIA DE LA LLANERIDAD</h1>
          <p class="text-lg">
            En el “día del Tributo a la Cultura Llanera” celebramos con orgullo
            la cultura, tradición e identidad llanera y resaltamos nuestra
            música y costumbres
          </p>
        </div>
        <div
          class="flex flex-row h-44 md:h-auto order-1 col-span-2 space-x-2 md:col-span-1 md:order-2"
        >
          <img
            src="/img/cultura-llanera-1.jpeg"
            alt=""
            class="max-h-80 w-full rounded-lg shadow-lg"
          />
        </div>
      </div>
      <div>2</div>
      <!-- <img class="" src="/img/cultura-llanera-2.jpg" alt="" />
        <img class="max-w-md" src="/img/cultura-llanera-3.jpg" alt="" /> -->
    </Stepper>
  </section>
</template>
