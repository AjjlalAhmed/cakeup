<script setup>
// Importing things we need
import { ref } from "@vue/reactivity";
import cake1 from "../assets/images/cake-1.png";
import cake4 from "../assets/images/cake-4.png";
import cake5 from "../assets/images/cake-5.png";

import cake8 from "../assets/images/cake-8.png";

// Variables
const data = ref([
  {
    id: 1,
    src: cake1,
    name: "Red velvet",
    price: "$22.00",
  },
  {
    id: 4,
    src: cake4,
    name: "Red velvet",
    price: "$24.00",
  },
  {
    id: 5,
    src: cake5,
    name: "Red velvet",
    price: "$52.00",
  },
  {
    id: 8,
    src: cake8,
    name: "Red velvet",
    price: "$11.00",
  },
]);
</script>

<template>
  <!-- Special  -->
  <div class="special">
    <!-- Title  -->
    <h1 class="title">special products</h1>
    <!-- Cards  -->
    <div class="cards">
      <!-- Card  -->
      <div v-for="item in data" :key="item.id" class="card">
        <!-- Image  -->
        <div class="img">
          <img loading="lazy" :src="item.src" alt="" />
        </div>
        <p class="name">{{ item.name }}</p>
        <p class="price">{{ item.price }}</p>
      </div>
    </div>
  </div>
  <!-- Special  -->
</template>

<style lang="scss" scoped>
.special {
  max-width: 1500px;
  margin: 150px auto;
  .title {
    text-transform: capitalize;
    font-size: 3rem;
    text-align: center;
    font-weight: 400;
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 40px;
    margin-top: 150px;
    .card {
      min-width: 300px;
      padding: 10px;
      border-radius: 5px;
      text-align: center;
      transition: 0.3s linear;
      border: 1px solid transparent;
      &:hover {
        border: 1px solid #b40b0b46;
      }
      cursor: pointer;

      .img {
        img {
          width: 250px;
          height: 250px;
          object-fit: fill;
        }
      }
      .name {
        font-size: 0.9rem;
        text-transform: capitalize;
        margin-top: 50px;
        text-align: center;
      }
      .price {
        font-size: 1rem;
        text-transform: capitalize;
        text-align: center;
        color: #b40b0b;
        letter-spacing: 1px;
        padding: 10px;
        font-weight: 700;
      }
    }
  }
}

@media only screen and (max-width: 400px) {
  .tranding {
    .title {
      font-size: 2rem;
    }
    .cards {
      .card {
        .img {
          img {
            width: 100%;
            height: 100%;
            object-fit: fill;
          }
        }
      }
    }
  }
}
</style>



