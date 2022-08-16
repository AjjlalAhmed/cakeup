<script setup>
// Importing things we need
import Navbar from "./components/Navbar.vue";

</script>


<template>
  <!-- Container  -->
  <div class="container mx-auto">
    <!-- Navbar  -->
    <Navbar />
    <!-- View  -->
    <router-view />
  </div>
  <!-- Container  -->
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Lora:wght@400;500;600;700&display=swap");
* {
  padding: 0;
  margin: 0;
  font-family: "Lora", serif;
}
</style>
