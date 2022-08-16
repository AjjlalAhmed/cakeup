<script setup>
// Importing things we need
import { ref } from "@vue/reactivity";
import shop1 from "../assets/images/shop-1.jpg";
import shop2 from "../assets/images/shop-2.jpg";
import shop3 from "../assets/images/shop-3.jpg";
// Variables
const data = ref([
  {
    id: 1,
    src: shop1,
    title: "cakeup shop",
    text: "party cakes",
  },
  {
    id: 2,
    src: shop2,
    title: "cakeup shop",
    text: "party cakes",
  },
  {
    id: 3,
    src: shop3,
    title: "cakeup shop",
    text: "party cakes",
  },
]);
</script>

<template>
  <!-- Shop  -->
  <div class="shop">
    <!-- Cards  -->
    <div class="cards">
      <!-- Card  -->
      <div v-for="item in data" :key="item.id" class="card">
        <!-- Image  -->
        <img loading="lazy" class="img" :src="item.src" alt="Sample 1" />
        <!-- Card wrapper -->
        <div class="card-wrapper">
          <!-- Info  -->
          <div class="info">
            <!-- Crd title  -->
            <h1 class="card-title">{{ item.title }}</h1>
            <!-- Card text  -->
            <p class="card-text">{{ item.text }}</p>
          </div>
        </div>
      </div>
      <!-- Card  -->
    </div>
  </div>
  <!-- Shop  -->
</template>



<style lang="scss" scoped>
.shop {
  max-width: 1500px;
  margin: 50px auto;
  
  .cards {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
    .card {
      cursor: pointer;
      position: relative;
      .img {
        width: 480px;
        height: 480px;
        object-fit: cover;
        filter: brightness(90%);
        border-radius: 5px;
      }
      .card-wrapper {
        display: grid;
        place-items: center;
        width: 100%;
        position: absolute;
        bottom: 50px;
        transition: 0.3s ease-in-out;
        .info {
          background: #fff;
          padding: 20px;
          border-radius: 5px;
          border: 1px solid #5555;
          transition: 0.3s ease-in-out;
          .card-title {
            text-align: center;
            font-size: 1rem;
            text-transform: capitalize;
            color: #b40b0b;
            font-weight: 400;
          }
          .card-text {
            text-align: center;
            font-size: 2rem;
            text-transform: capitalize;
          }
        }
      }

      &:hover > .card-wrapper > .info {
        background: #b40b0b;
        .card-title {
          color: #fff;
        }
        .card-text {
          color: #fff;
        }
      }
    }
  }
}

// Media queries

@media only screen and (max-width: 1520px) {
  .shop {
    .cards {
      justify-content: center;
    }
  }
}
@media only screen and (max-width: 500px) {
  .shop {
    .cards {
      .card {
        .img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          filter: brightness(90%);
        }
      }
    }
  }
}
</style>