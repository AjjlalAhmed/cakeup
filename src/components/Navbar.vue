<script setup>
// Importing things we need
import { ref } from "@vue/reactivity";
import logoImg from "../assets/images/logo.png";

// Variables
const showMenu = ref(false);

// Functions
const toggleNavbar = () => (showMenu.value = !showMenu.value);
</script>



<template>
  <!-- Header -->
  <header class="header">
    <!-- Nav  -->
    <nav class="nav">
      <!-- Logo  -->
      <div class="logo">
        <img :src="logoImg" alt="Logo" />
      </div>
      <!-- Nav ul  -->
      <ul :class="{ 'nav-ul': true, hide: showMenu }">
        <!-- Item  -->
        <li class="item">
          <!-- Link  -->
          <router-link to="#" class="link">home</router-link>
        </li>
        <!-- Item  -->
        <li class="item">
          <!-- Link  -->
          <router-link to="#" class="link">categories</router-link>
        </li>
        <!-- Item  -->
        <li class="item">
          <!-- Link  -->
          <router-link to="#" class="link">special</router-link>
        </li>
        <!-- Item  -->
        <li class="item">
          <!-- Link  -->
          <router-link to="#" class="link">contact</router-link>
        </li>
      </ul>
      <!-- Action buttons  -->
      <div :class="{ 'action-btns': true, hide: showMenu }">
        <div class="input">
          <label for="search"
            ><i class="fa fa-search" aria-hidden="true"></i
          ></label>
          <input id="search" type="text" placeholder="Search" />
        </div>
        <button>
          <i class="fa fa-shopping-cart" aria-hidden="true"></i> cart
        </button>
        <button><i class="fa fa-user" aria-hidden="true"></i> user</button>
      </div>
      <!-- Menu  -->
      <div @click="toggleNavbar" class="menu">
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
      </div>
    </nav>
  </header>
  <!-- Header -->
</template>


<style lang="scss" scoped>
.header {
  padding: 20px;
  .nav {
    display: flex;
    justify-content: space-between;
    max-width: 1500px;
    margin: auto;
    .logo {
      justify-self: left;
      img {
        width: 80px;
      }
    }
    .nav-ul {
      display: flex;
      align-self: center;
      justify-content: center;
      margin-left: 10%;
      .item {
        list-style: none;
        padding: 20px;
        .link {
          display: inline-block;
          text-decoration: none;
          font-size: 1rem;
          letter-spacing: 1px;
          text-transform: capitalize;
          transition: 0.3s ease-in-out;
          position: relative;
          color: #000;
        }

        .link:after {
          content: "";
          position: absolute;
          width: 100%;
          transform: scaleX(0);
          height: 2px;
          bottom: 0;
          left: 0;
          transform-origin: bottom right;
          transition: transform 0.25s ease-out;
          background-color: #b40b0b;
        }

        .link:hover:after {
          transform: scaleX(1);
          transform-origin: bottom left;
        }
      }
    }
    .action-btns {
      display: flex;
      align-items: center;
      justify-self: right;
      gap: 20px;
      .input {
        // border: 1px solid #3333;
        padding: 5px;
        border-radius: 5px;
        label {
          font-size: 1rem;
          text-transform: capitalize;
          color: #b40b0b;
          margin: 0 5px;
        }
        input {
          border: 0px;
          max-width: 90px;
             font-size: 1rem;
          &:focus {
            outline: none;
          }
        }
      }
      button {
        font-size: 0.9rem;
        text-transform: capitalize;
        background: transparent;
        border: 0px;
        i {
          color: #b40b0b;
        }
      }
    }
    .menu {
      display: none;
      .bar {
        display: block;
        background: #b40b0b;
        width: 30px;
        height: 3px;
        margin: 5px;
      }
    }
  }
}

// Media queries
@media only screen and (max-width: 990px) {
  .header {
    padding-bottom: 0px;
    .nav {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      .logo {
        grid-column: 1 / 3;
        grid-row: 1 / 2;
        justify-self: left;
        align-self: center;
      }
      .menu {
        display: block;
        grid-column: 3 / 4;
        grid-row: 1 / 2;
        justify-self: right;
        align-self: center;
      }
      .nav-ul {
        flex-direction: column;
        grid-column: 1 / 4;
        grid-row: 2 / 3;
        justify-self: center;
        height: 0;
        overflow: hidden;
        padding: 0;
        transition: 0.3s ease-in-out;
        width: 100%;
        margin:10px auto;
        text-align: center;
      
      }
      .action-btns {
        display: none;
      }
    }
  }
  .hide {
    height: 300px !important;
    background-color: #ffffff;
background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='4' height='4' viewBox='0 0 4 4'%3E%3Cpath fill='%23b40b0b' fill-opacity='0.4' d='M1 3h1v1H1V3zm2-2h1v1H3V1z'%3E%3C/path%3E%3C/svg%3E");
    border-radius: 5px;

    .item:first-child {
      padding-top: 40px !important;
    }
    .item:last-child {
      padding-bottom: 40px !important;
    }
  }
}
</style>