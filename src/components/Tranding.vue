<script setup>
// Importing things we need
import { ref } from "@vue/reactivity";
import cake1 from "../assets/images/cake-1.png";
import cake2 from "../assets/images/cake-2.png";
import cake3 from "../assets/images/cake-3.png";
import cake4 from "../assets/images/cake-4.png";
import cake5 from "../assets/images/cake-5.png";
import cake6 from "../assets/images/cake-6.png";
import cake7 from "../assets/images/cake-7.png";
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
    id: 2,
    src: cake2,
    name: "Red velvet",
    price: "$12.00",
  },
  {
    id: 3,
    src: cake3,
    name: "Red velvet",
    price: "$21.00",
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
    id: 6,
    src: cake6,
    name: "Red velvet",
    price: "$23.00",
  },
  {
    id: 7,
    src: cake7,
    name: "Red velvet",
    price: "$22.00",
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
  <!-- Tranding  -->
  <div class="tranding">
    <!-- Title  -->
    <h1 class="title">tranding products</h1>
    <!-- Cards  -->
    <div class="cards">
      <!-- Card  -->
      <div v-for="item in data" :key="item.id" class="card">
        <!-- Image  -->
        <div class="img">
          <img loading="lazy" :src="item.src" alt="" />
        </div>
        <!-- Name  -->
        <p class="name">{{ item.name }}</p>
        <!-- Price  -->
        <p class="price">{{ item.price }}</p>
      </div>
      <!-- Card  -->
    </div>
    <!-- Cards  -->
  </div>
  <!-- Tranding  -->
</template>

<style lang="scss" scoped>
// Styles
.tranding {
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
      box-shadow: rgba(0, 0, 0, 0.05) 0px 6px 24px 0px,
        rgba(0, 0, 0, 0.08) 0px 0px 0px 1px;
      background: #fcf9f4;
      &:nth-child(even) {
        background: #f7f7f7;
      }
      &:hover {
        border: 1px solid #fce7e7;
        box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
      }
      cursor: pointer;

      .img {
        img {
          width: 250px;
          height: 250px;
          object-fit: contain;
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

// Media queries

@media only screen and (max-width: 500px) {
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
            max-width: 250px;
          }
        }
      }
    }
  }
}
</style>



