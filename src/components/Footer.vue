<script setup>
</script>

<template>
  <!-- Footer  -->
  <footer class="footer">
    <!-- Wrapper  -->
    <div class="wrapper">
      <!-- Title  -->
      <h1 class="title">Contact</h1>
      <!-- Text  -->
      <p class="text">
        Cakeup's Cakes is Karachi's oldest and pioneer customized cake place
        which offers a comprehensive range of cake flavours and types for every
        occasion such as edible picture cakes, 3D Theme Cakes, Butter Cream
        Themed Cakes, Heart-shaped cakes, cartoon character cakes, black forest
        cake, chocolate cakes as well as Truffles, Flowers, Assorted Date Gift
        Box, Bread Baskets, Bread Platters, Ramadan Platter, Eid Platters, Eid
        Gift Box and many more.
      </p>
      <!-- Contact  -->
      <div class="contact">
        <!-- left  -->
        <section class="left">
          <!-- Info  -->
          <ul>
            <li>Street: Strandgaten 83, 5004 Bergen, Norway</li>
            <li>Phone: 1,447,777,7772</li>
            <li>Email: support@cakeup.com</li>
          </ul>
        </section>
        <!-- Rigth  -->
        <section class="rigth">
          <!-- Map  -->
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1970.992468320644!2d5.315204416190199!3d60.395802232098575!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x463cfd9aa2e945dd%3A0xcfdfa56f6b705584!2sCakeup%20AS!5e0!3m2!1sen!2s!4v1660744392899!5m2!1sen!2s"
            style="border: 0"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </section>
      </div>
    </div>
    <!-- Bottom bar -->
    <div class="bottom-bar">
      <p>copyright &copy;2022 Cakeup</p>
    </div>
  </footer>
  <!-- Footer  -->
</template>



<style lang="scss" scoped>
// Styles
.footer {
  background: #fcf9f4;
  .map {
    width: 100%;
    border-radius: 5px;
    overflow: hidden;
    iframe {
      width: 100%;
      min-height: 500px;
    }
  }
  .wrapper {
    max-width: 1500px;
    margin: auto;
    .title {
      text-transform: capitalize;
      font-size: 3rem;
      text-align: center;
      font-weight: 400;
      padding: 0px 5px;
      padding-top: 40px;
    }
    .text {
      max-width: 800px;
      margin: 40px auto;
      text-align: center;
      font-size: 1.2rem;
      letter-spacing: 1px;
      line-height: 2rem;
      padding: 0px 5px;
    }
    .contact {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap-reverse;
      align-items: center;
      padding: 20px 0px;
      gap: 20px;
      padding: 20px;
      .rigth {
        iframe {
          width: 100%;
          min-width: 800px;
          min-height: 500px;
        }
      }
      .left {
        ul {
          list-style: none;
          li {
            font-size: 1.2rem;
            padding: 10px;
            letter-spacing: 1px;
          }
        }
      }
    }
  }
  .bottom-bar {
    background: #b40b0b;
    padding: 10px;
    color: #fff;
    font-size: 1.2rem;
    text-align: center;
    text-transform: capitalize;
    letter-spacing: 1px;
  }
}

// Medai queries
@media only screen and (max-width: 1230px) {
  .footer {
    .wrapper {
      .contact {
        flex-direction: column;
        align-items: center;
        gap: 20px;
      }
    }
  }
}
@media only screen and (max-width: 850px) {
  .footer {
    .wrapper {
      .contact {
        .rigth {
          width: 100%;
          iframe {
            width: 100%;
            min-width: 100%;
            min-height: 500px;
          }
        }
      }
    }
  }
}
</style>