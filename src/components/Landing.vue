<script setup>
// Importing things we need
import { Splide, SplideSlide, SplideTrack } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";
import { ref } from "@vue/reactivity";
import landing1 from "../assets/images/lg-1.jpg";
import landing2 from "../assets/images/lg-2.jpg";
import landing3 from "../assets/images/lg-3.jpg";

// Variables
const data = ref([
  {
    id: 1,
    src: landing1,
    title: "best cake shop",
    text: "Looking to satisfy your sweet-toothed cravings?",
  },
  {
    id: 2,
    src: landing2,
    title: "The cake master",
    text: "Delizia bakery is arguably the best bakery in town",
  },
  {
    id: 3,
    src: landing3,
    title: "Famous for its flavor and quality",
    text: "our customer service is absolutely exquisite.",
  },
]);


</script>

<template>
  <!-- Landing  -->
  <div class="landing">
    <!-- Splide  -->
    <Splide class="wrapper" :options="{ rewind: true }">
      <!-- SplideSlide  -->
      <SplideSlide v-for="item in data" :key="item.id">
        <!-- Image  -->
        <img class="slide-img" :src="item.src" alt="Sample 1" />
        <!-- Card  -->
        <div class="card">
          <div class="card-wrapper">
            <!-- Crd title  -->
            <h1 class="card-title">{{ item.title }}</h1>
            <!-- Card text  -->
            <p class="card-text">{{ item.text }}</p>
          </div>
        </div>
      </SplideSlide>
    </Splide>
   <!-- Splide  -->
  </div>
  <!-- Landing  -->
</template>

<style lang="scss" scoped>
.landing {
  max-width: 1500px;
  margin: auto;
  .wrapper {
    position: relative;
    .slide-img {
      width: 100%;
      max-height: 800px;
      height: 100%;
      min-height: 70vh;
      object-fit: cover;
      border-radius: 5px;
      filter: brightness(90%);
    
    }
    .card {
      display: grid;
      place-items: center;
      width: 100%;
      position: absolute;
      bottom: 30px;
      .card-wrapper {
        background: #fff;
        padding: 20px;
        border-radius: 5px;
        border: 1px solid #5555;
        .card-title {
          text-align: center;
          font-size: 2rem;
          text-transform: capitalize;
        }
        .card-text {
          text-align: center;
          font-size: 1rem;
        }
      }
    }
  }
}

// Media queries
@media only screen and (max-width: 670px) {
  .landing {
    .wrapper {
      .card {
        display: none;
      }
    }
  }
}
</style>