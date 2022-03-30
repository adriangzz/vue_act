<script setup lang="ts">
const persons = [
  { name: "adrian", age: 24 },
  { name: "david", age: 20 },
  { name: "catalina", age: 20 },
  { name: "jose", age: 18 },
];
</script>

<template>
  <h3>Persons:</h3>
  <li v-for="person in persons">
    <div>
      <p>Nombre: {{ person.name }}</p>
      <p>Edad: {{ person.age }}</p>
    </div>
  </li>
</template>

<style scoped>
h3 {
  margin-top: 2rem;
}
li {
  margin-top: 1rem;
}
</style>
