<script setup lang="ts">
import { ref } from "vue";

const name = ref("");
</script>

<template>
  <input type="text" placeholder="Your Name" v-model="name" />
  <p v-if="name">Hello {{ name }}</p>
  <p v-else>Write your name in the input!</p>
</template>

<style scoped>
input {
  margin-top: 2rem;
  display: block;
}

p {
  font-size: 1.5rem;
}
</style>
