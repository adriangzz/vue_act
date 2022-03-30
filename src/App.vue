<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="wrapper">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<style>
@import "./assets/base.css";

#app {
  margin: 2rem;
}

header {
  position: fixed;
  display: flex;
  right: 2rem;
  z-index: 9;
}
a {
  display: block;
  color: white;
}
</style>
