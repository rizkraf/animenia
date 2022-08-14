<template>
  <header class="bg-white">
    <div class="container mx-auto flex items-center justify-between py-6">
      <h2 class="text-red-600 text-2xl font-bold">Animenia</h2>
      <!-- <nav class="flex items-center">
        <NuxtLink to="/anime">All</NuxtLink>
      </nav> -->
      <div
        class="max-w-[192px] w- w-full flex items-center gap-2 bg-neutral-100 px-3 py-2 rounded-lg"
      >
        <span>
          <IconSearch class="text-neutral-500 h-5 w-5" />
        </span>
        <input
          type="text"
          class="bg-transparent w-full text-sm text-neutral-500 placeholder-neutral-500 focus:border-none focus:outline-none"
          placeholder="Search..."
        />
      </div>
    </div>
  </header>
</template>
