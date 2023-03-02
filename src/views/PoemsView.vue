
<script setup>
import poemsJson from './poems.json'
</script>

<template>
  <div class =" flex flex-col px-5 pt-8 pb-10 items-center">
    <h1 class=" text-2xl text-green-700 font-bold">List of Poems</h1>
    <br>
    
    <div>
      <div v-for="poem in poemsJson.poems" :key="poem.id">
        <RouterLink v-bind:to="'/poems/' + poem['id']">
          <h1 class=" text-lg underline hover:text-blue-600">{{ poem['title-en'] }}</h1>
        </RouterLink>
        <p>{{ poem.year }}</p>
        <br>
      </div>
    </div>
  </div>
</template>

<style scoped>
.body {
  background-color: rgb(187, 187, 251);
}

button {
  
}
</style>