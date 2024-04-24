<template>
  <div
    class="relative w-full h-dvh bg-fixed bg-no-repeat bg-cover bg-center"
    :style="{
      backgroundImage: 'url(/img/cultura-llanera-1.jpeg)',
      clipPath: 'polygon(0 0, 100% 0, 100% 85%, 50% 100%, 50% 100%, 0 85%)',
    }"
  >
    <div class="absolute w-full h-full backdrop-blur-sm bg-black/30" />
    <div class="relative h-full">
      <div class="flex flex-col items-center justify-center drop-shadow-md">
        <h1 class="mx-auto text-6xl text-center text-white mt-52">
          <p>Día del tributo a la</p>
          <strong class="font-bold text-8xl">Cultura Llanera</strong>
        </h1>
        <p class="flex gap-4 text-lg text-white mt-4">
          <span>26 abril</span>
          <span>2:00 pm a 6:00 pm</span>
          <span>Colegio Luis Carlos Galan</span>
        </p>
        <img
          class="mt-28"
          src="/img/logo-alcaldia.png"
          alt="logo-alcaldia-acacias"
        />
      </div>
    </div>
  </div>
</template>
