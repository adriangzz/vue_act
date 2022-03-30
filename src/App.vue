<script setup lang="ts">
import Title from "./components/Title.vue";
import Image from "./components/Image.vue";
import HelloName from "./components/HelloName.vue";
import Arrays from "./components/Arrays.vue";
import Hide from "./components/Hide.vue";
</script>

<template>
  <header>
    <div class="wrapper"></div>
  </header>

  <main>
    <Title title="Pets App" />
    <Image />
    <HelloName />
    <Arrays />
    <Hide />
  </main>
</template>

<style>
@import "./assets/base.css";

#app {
  margin: 2rem;
}
</style>
