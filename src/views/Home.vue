<script setup>
// Importing things we need
import Landing from "../components/Landing.vue";
import Shop from "../components/Shop.vue";
import Tranding from "../components/Tranding.vue";
import Testimonial from "../components/Testimonial.vue";
import Special from "../components/Special.vue";
import See from "../components/See.vue";
</script>

<template>
  <!-- Home  -->
  <div class="home">
    <!-- Landing  -->
    <Landing />
    <!-- Shop  -->
    <Shop />
    <!-- Tranding  -->
    <Tranding />
    <!-- Testimonial  -->
    <Testimonial />
    <!-- Special -->
    <Special />
    <!-- See  -->
    <See />
  </div>
  <!-- Home  -->
</template>

<style lang="scss" scoped>
.home {
  padding: 0px 20px;
}
</style>

