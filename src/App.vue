<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
import Title from "./components/Title.vue";
</script>

<template>
  <header>
    <div class="wrapper"></div>
  </header>

  <main>
    <Title title="Pets App" />
  </main>
</template>

<style>
@import "./assets/base.css";

#app {
  margin: 2rem;
}
</style>
