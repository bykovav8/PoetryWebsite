
<script setup>
import poemsJson from './poems.json'
</script>

<template>
  <div id="poems-list">
    <h1 class=" text-2xl text-green-700 font-bold">List of Poems</h1>
    <br>
    <div v-for="poem in poemsJson.poems" :key="poem.id">
      <RouterLink v-bind:to="'/poems/' + poem['id']">
        <h1 class=" text-lg underline">{{ poem['title-en'] }}</h1>
      </RouterLink>
      <p>{{ poem.year }}</p>
      <br>
    </div>
  </div>
</template>

<style scoped>
.body {
  background-color: rgb(187, 187, 251);
}
</style>