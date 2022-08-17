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
    <!-- Wrapper  -->
    <div class="wrapper">
      <!-- Title  -->
      <h1 class="title">ours testimonial</h1>
      <!-- Splide  -->
      <Splide :options="{ rewind: true }">
        <!-- SplideSlide  -->
        <SplideSlide v-for="item in data" :key="item.id">
          <!-- Card  -->
          <div class="card">
            <!-- Card text  -->
            <p class="card-text">{{ item.text }}</p>
            <!-- Card auther  -->
            <p class="card-auther">{{ item.auther }}</p>
            <br />
          </div>
        </SplideSlide>
      </Splide>
      <!-- Splide  -->
    </div>
    <!-- Wrapper  -->
  </div>
  <!-- Testimonial -->
</template>



<style lang="scss" scoped>
// Styles
.testimonial {
  max-width: 1500px;
  margin: 20px auto;
  padding: 100px 20px;
  background: url("../assets/images/testimonial.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  border-radius: 5px;
  overflow: hidden;

  .title {
    text-transform: capitalize;
    font-size: 3rem;
    text-align: center;
    font-weight: 400;
  }
  .wrapper {
    margin: 30px 0px;
    background-color: #fcf9f4;
    box-shadow: rgba(0, 0, 0, 0.02) 0px 1px 3px 0px,
      rgba(27, 31, 35, 0.15) 0px 0px 0px 1px;
    border-radius: 5px;
    padding: 40px 20px;
  }
  .card {
    text-align: center;
    max-width: 800px;
    margin: auto;
    padding: 20px 0px;
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
    }
  }
}

// Media queries

@media only screen and (max-width: 500px) {
  .testimonial {
    padding: 100px 5px;
    .title {
      font-size: 2rem;
    }
  }
}
</style>

<style lang="scss">
.testimonial {
  .wrapper {
    .splide {
      .splide__arrow {
        display: none !important;
      }
    }
  }
}
</style>