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
  <img :src="img" v-if="img" alt="" />
  <button @click="changeImage" :disabled="disabled">Change Image</button>
</template>

<style scoped>
img {
  width: 28rem;
}
button {
  display: block;
}
</style>
