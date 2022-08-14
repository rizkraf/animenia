<template>
  <div
    class="flex items-center gap-3 bg-white mb-6 p-5 rounded-lg shadow-md shadow-neutral-200/30"
  >
    <div class="bg-red-600 p-1.5 inline-block rounded-md">
      <IconImage class="h-4 w-4 text-white" />
    </div>
    <h2 class="text-lg text-red-600 font-medium">
      <slot />
    </h2>
  </div>
</template>
