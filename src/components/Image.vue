<script setup lang="ts">
import { ref } from "vue";
import { onMounted } from "vue";

const img = ref("");
const disabled = ref(true);

const changeImage = async () => {
  disabled.value = true;
  const image = await fetch(" https://dog.ceo/api/breeds/image/random");
  const imgSrc = await image.json();
  img.value = imgSrc.message;
  disabled.value = false;
};

onMounted(() => {
  changeImage();
});
</script>

<template>
  <div class="card">
    <img :src="img" v-if="img" alt="" />
    <p v-else="img">Loading image</p>
    <button @click="changeImage" :disabled="disabled">Change Image</button>
  </div>
</template>

<style scoped>
.card {
  display: inline-block;
  background-color: #202020;
  padding: 2rem;
  border-radius: 1rem;
}
img {
  width: 28rem;
}
button {
  display: block;
}
</style>
