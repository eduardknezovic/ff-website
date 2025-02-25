<template>
  <div class="container">
    <h1>Flash Fluency</h1>
    <p>Goodbye default sadness, hello custom happiness!</p>
    
    <!-- NuxtUI Components -->
    <UCard class="my-4">
      <template #header>
        <div class="flex items-center justify-between">
          <h3 class="text-lg font-semibold">NuxtUI Card Example</h3>
          <UBadge color="primary">New</UBadge>
        </div>
      </template>
      <p>This is a card component from NuxtUI library.</p>
      <template #footer>
        <div class="flex justify-end gap-2">
          <UButton color="gray" variant="ghost">Cancel</UButton>
          <UButton color="primary">Submit</UButton>
        </div>
      </template>
    </UCard>

    <div class="flex flex-col gap-4 my-6">
      <UAlert title="Information" color="blue" icon="i-heroicons-information-circle">
        This is an informational alert from NuxtUI.
      </UAlert>
      
      <UInput placeholder="Type something..." icon="i-heroicons-magnifying-glass" />
      
      <USelect
        :options="['Option 1', 'Option 2', 'Option 3']"
        placeholder="Select an option"
      />
      
      <UToggle v-model="toggleState" />
    </div>
    
    <!-- Example of using Nuxt's built-in components -->
    <NuxtLink to="/">Back to Home</NuxtLink>
  </div>
</template>

<script setup>
// Your component logic goes here
import { ref } from 'vue'

const toggleState = ref(false)
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
}
</style>

