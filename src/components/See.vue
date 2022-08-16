<script setup>
// Importing things we need
</script>

<template>
  <!-- See  -->
  <div class="see">
    <!-- Title  -->
    <h1 class="title">we can't see you</h1>
  </div>
  <!-- See  -->
</template>



<style lang="scss" scoped>
.see {
  display: grid;
  place-items: center;
  max-width: 1500px;
  margin:50px auto;
  background: url("../assets/images/see.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 500px;
  border-radius: 5px;
  .title {
    text-transform: capitalize;
    font-size: 3rem;
    text-align: center;
    border-radius: 5px;
    border: 1px solid #5555;
    color: #000;
    position: relative;
    z-index: 2;
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='4' height='4' viewBox='0 0 4 4'%3E%3Cpath fill='%23b40b0b' fill-opacity='0.4' d='M1 3h1v1H1V3zm2-2h1v1H3V1z'%3E%3C/path%3E%3C/svg%3E");
    padding: 50px;
    border-radius: 5px;
    font-weight: 400;
  }
}

// Media queries
@media only screen and (max-width: 565px) {
  .see {
    .title {
      font-size: 1.5rem;
      padding: 20px;
    }
  }
}
</style>