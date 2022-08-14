<script setup>
const { data: seasonal } = await useFetch(
  "https://api.jikan.moe/v4/seasons/now"
);

const seasonalFiltered = computed(() => seasonal.value.data.slice(0, 5));
</script>

<template>
  <main class="my-12">
    <div class="container mx-auto">
      <SectionWrapper id="season" class="mb-12">
        <SectionHeader>Summer Season</SectionHeader>
        <SectionBody>
          <CardAnime
            v-for="anime in seasonalFiltered"
            :key="anime.mal_id"
            :anime="anime"
          />
        </SectionBody>
      </SectionWrapper>

      <SectionWrapper id="top-100">
        <SectionHeader>Top 100</SectionHeader>
      </SectionWrapper>
    </div>
  </main>
</template>
