<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import MainHero from './components/MainHero.vue';
import Projects from './components/Projects.vue';
import NavBar from './components/NavBar.vue';
</script>

<template>
  <NavBar />
  <MainHero />
  <Projects />
   
</template>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  
}
</style>
