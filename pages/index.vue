
<template>
  <div class="container">
    <h1>My New Nuxt Page</h1>
    <p>Goodbye default sadness, hello custom happiness!</p>
    
    <!-- Example of using Nuxt's built-in components -->
    <NuxtLink to="/">Back to Home</NuxtLink>
  </div>
</template>

<script setup>
// Your component logic goes here
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

