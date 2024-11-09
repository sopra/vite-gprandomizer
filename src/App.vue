<script setup>
import GPHeaderVue from './components/GPHeader.vue'
import GPRandomizerBoardVue from './components/GPRandomizerBoard.vue'
import GPFooter from './components/GPFooter.vue';
</script>

<template>
  <v-app>
    <GPHeaderVue />
    <GPRandomizerBoardVue />
    <GPFooter />
  </v-app>
</template>

<style scoped>
/*
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
  */
</style>
