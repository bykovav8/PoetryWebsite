<script setup>
import { RouterLink, useRoute } from 'vue-router';
import { computed, normalizeClass, ref } from 'vue';

const route = useRoute();
const isHome = computed(() => {
  return route.name === "home";
});

const isAbout = computed(() => {
  return route.name === "about";
});

const isPoems = computed(() => {
  return route.name === "poems";
});

</script>

<template>
  <div class=" flex justify-start bg-green-600 text-white py-3.5 text-lg shadow-lg shadow-slate-400">
    <span class=" px-2">
      <RouterLink to="/">
        <button class="nav-button px-2 py-1 hover:text-gray-300 border-none" v-bind:class="isHome && 'bg-blue-400'">
          Home
        </button>
      </RouterLink>
    </span>
    <span class=" px-2">
      <RouterLink to="/about">
        <button class="nav-button px-2 py-1" v-bind:class="isAbout && 'bg-blue-400'">
          About
        </button>
      </RouterLink>
    </span>
    <span class=" px-2">
      <RouterLink to="/poems">
        <button class="nav-button px-2 py-1" v-bind:class="isPoems && 'bg-blue-400'">
          Poems
        </button>
      </RouterLink>
    </span>
  </div>
</template>

<style scoped>
  .nav-button {
    border: none;
    transition: all 0.3s ease;
  }

  .nav-button:hover {
    color: rgb(219, 219, 219);
    transform: translate(0, 1px)
  }

  .nav-button.bg-blue-400 {
    color: white;
    transform: translate(0, 0);
  }
  
</style>