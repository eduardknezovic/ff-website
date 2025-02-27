<template>
  <ContentRenderer v-if="home" :value="home" />
  <div v-else>Home not found</div>
</template>

<script setup lang="ts">
const { data: home } = await useAsyncData(() => queryCollection('content').path('/').first())

useSeoMeta({
  title: home.value?.title,
  description: home.value?.description
})
</script>

<style>
/* Removed 'scoped' to allow styles to affect content from ContentRenderer */

h1 {
  @apply text-4xl font-bold;
}

h2 {
  @apply text-2xl font-bold;
}

p {
  @apply text-lg;
}

</style>
