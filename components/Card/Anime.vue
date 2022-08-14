<script setup>
const props = defineProps({
  anime: {
    type: Object,
    default: {},
  },
});
</script>

<template>
  <div class="relative overflow-hidden rounded-lg">
    <img
      :src="props.anime.images.jpg.image_url"
      class="relative w-full h-full"
      :alt="props.anime.title"
    />
    <div
      class="absolute bottom-0 left-0 right-0 h-20 bg-white/90 backdrop-blur p-4"
    >
      <h3 class="text-red-600 font-medium">
        {{
          props.anime.title.length > 25
            ? props.anime.title.slice(0, 20) + "..."
            : props.anime.title
        }}
      </h3>
      <p class="text-xs text-neutral-500">
        <template v-for="genre in props.anime.genres" :key="genre.mal_id">
          {{ genre.name + " " }}
        </template>
      </p>
    </div>
  </div>
</template>
