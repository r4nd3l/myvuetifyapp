<template>
  <h1 class="text-2xl font-bold text-blue-600">{{ msg }}</h1>
</template>

<script setup lang="ts">
defineProps<{ msg: string }>();
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
