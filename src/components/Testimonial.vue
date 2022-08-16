<script setup>
// Importing things we need
import { ref } from "@vue/reactivity";
import { Splide, SplideSlide, SplideTrack } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

// Variables
const data = ref([
  {
    id: 1,
    text: "I had Sweet Themes create my beautiful wedding cake and I must say I was completely satisfied! Not only was it beautiful but it was also delicious! Thank you so much Sweet Themes for making my wedding that much sweeter!",
    auther: "jonh doe",
  },
  {
    id: 2,
    text: "I had Sweet Themes create my beautiful wedding cake and I must say I was completely satisfied! Not only was it beautiful but it was also delicious! Thank you so much Sweet Themes for making my wedding that much sweeter!",
    auther: "mike wilson",
  },
  {
    id: 3,
    text: "I had Sweet Themes create my beautiful wedding cake and I must say I was completely satisfied! Not only was it beautiful but it was also delicious! Thank you so much Sweet Themes for making my wedding that much sweeter!",
    auther: "maria bun",
  },
]);
</script>

<template>
  <!-- Testimonial -->
  <div class="testimonial">
    <!-- Title  -->
    <h1 class="title">ours testimonial</h1>
    <!-- Splide  -->
    <Splide class="wrapper" :options="{ rewind: true }">
      <!-- SplideSlide  -->
      <SplideSlide v-for="item in data" :key="item.id">
        <!-- Card  -->
        <div class="card">
          <!-- Card text  -->
          <p class="card-text">{{ item.text }}</p>
          <p class="card-auther">{{ item.auther }}</p>
        </div>
      </SplideSlide>
    </Splide>
    <!-- Splide  -->
  </div>
  <!-- Testimonial -->
</template>



<style lang="scss" scoped>
.testimonial {
  max-width: 1500px;
  margin: 20px auto;
  padding: 50px 0px;
  background-color: #ffffff;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='4' height='4' viewBox='0 0 4 4'%3E%3Cpath fill='%23b40b0b' fill-opacity='0.4' d='M1 3h1v1H1V3zm2-2h1v1H3V1z'%3E%3C/path%3E%3C/svg%3E");
  border-radius: 5px;
  .title {
    text-transform: capitalize;
    font-size: 3rem;
    text-align: center;
    font-weight: 400;
  }
  .wrapper {
    margin-top: 50px;
  }
  .card {
    text-align: center;
    max-width: 800px;
    margin: auto;
    .card-text {
      font-size: 1.2rem;
      letter-spacing: 1px;
      padding: 10px;
    }
    .card-auther {
      font-size: 1.2rem;
      letter-spacing: 1px;
      color: #b40b0b;
      font-weight: 700;
      text-transform: capitalize;
      padding-bottom: 50px;
    }
  }
}
</style>