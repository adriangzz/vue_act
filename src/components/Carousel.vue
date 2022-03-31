<script setup lang="ts">
import { ref } from "vue";

const idx = ref(0);

const images = [
  new URL("../assets/5200.jpg", import.meta.url).href,
  new URL("../assets/cat-and-dog-happy.jpg", import.meta.url).href,
];

const changeImage = () => {
  if (idx.value == images.length - 1) {
    idx.value = 0;
  } else {
    idx.value = idx.value += 1;
  }
};
</script>

<template>
  <div class="card">
    <h2>Carousel</h2>
    <img :src="images[idx]" alt="" />
    <button @click="changeImage">next</button>
  </div>
</template>

<style scoped>
.card {
  display: block;
  margin-top: 2rem;
}
</style>
