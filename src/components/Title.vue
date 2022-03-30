<script setup lang="ts">
defineProps<{
  title: string;
}>();
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ title }}</h1>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}
</style>
