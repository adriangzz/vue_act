<script setup lang="ts">
import { ref } from "vue";

const hide = ref(false);

const hideText = () => {
  hide.value = !hide.value;
};
</script>

<template>
  <button @click="hideText" v-if="!hide">Hide</button>
  <button @click="hideText" v-else="hide">Unhide</button>
  <p v-if="!hide">This is not hidden!</p>
</template>

<style scoped>
button {
  margin-top: 2rem;
}
</style>
