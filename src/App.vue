<template>
  <v-app>
    <v-main class="p-6">
      <textTitle msg="Hello Vue + Tailwind + Vuetify 🚀" />
      <v-btn color="primary">Vuetify Button</v-btn>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
import textTitle from "./components/testTitle.vue";
</script>

<style scoped>
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
</style>
