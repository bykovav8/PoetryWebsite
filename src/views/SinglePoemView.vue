<script setup>
import poemsJson from './poems.json';
import { useRoute } from 'vue-router';
const route = useRoute();

let curPoem = poemsJson.poems[route.params.id];

</script>

<template>
  <RouterLink to="/poems">
    <button class="w-16 text-lg bg-blue-300 absolute ml-2 mt-2">
      Back
    </button>
  </RouterLink>
  <div class=" text-center mt-10 pb-10">
    <h1 class=" text-xl font-bold">{{ curPoem['title-en'] }}</h1>
    <div v-for="verse in curPoem['poem-en']" :key="curPoem.id">
      <br>
      <p v-for="line in verse" :key="curPoem.id"> {{ line }} </p>
    </div>
    <br>
    <p>{{ curPoem['year'] }}</p>
  </div>
</template>