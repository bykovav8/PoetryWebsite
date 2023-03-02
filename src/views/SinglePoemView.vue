<script setup>
import poemsJson from './poems.json';
import { useRoute } from 'vue-router';
const route = useRoute();

let curPoem = poemsJson.poems[route.params.id];

</script>

<template>
  <div class=" text-center">
    <h1 class=" text-xl top-1 font-bold">{{ curPoem['title-en'] }}</h1>
    <div v-for="verse in curPoem['poem-en']" :key="curPoem.id">
      <br>
      <p v-for="line in verse" :key="curPoem.id"> {{ line }} </p>
    </div>
    <br>
    <p>{{ curPoem['year'] }}</p>
  </div>
</template>