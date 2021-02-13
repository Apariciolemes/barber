<template>
  <div class="home-page">
    <div class="home-page__upper">
      <div class="container">
        <div class="home-page__upper__logo">
          <router-link to="/">
            <img src="@/assets/images/barbershoplogo.png" />
          </router-link>
        </div>
        <div class="home-page__upper__access">
          <div class="home-page__upper__access__client">
            <h3>Cliente</h3>
            <img src="@/assets/images/cliente.svg" />
          </div>
          <div class="home-page__upper__access__barber">
            <h3>Barbeiro</h3>
            <img src="@/assets/images/barbeiro.png" />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Footer from "../footer/Footer.vue";

@Component({
  components: { Footer },
})
export default class Home extends Vue {
  mounted() {
    console.log("hello");
  }
}
</script>


<style lang="scss">
.home-page {
  &__upper {
    background: url("../../assets/images/fundo.jpg") no-repeat;
    background-size: cover;
    width: 100%;
    height: 85vh;
    &__logo {
      padding-top: 25px;

      img {
        width: 180px;
        cursor: pointer;
      }

      img:hover {
        -moz-transform: scale(1.1);
        -webkit-transform: scale(1.1);
        transform: scale(1.1);
      }
    }

    &__access {
      display: flex;
      align-items: flex-end;
      justify-content: center;

      h3 {
        text-align: center;
        color: #fff;
        font-weight: 900;
        font-size: 30px;
        text-transform: uppercase;
        text-decoration: underline;
      }
      img {
        width: 200px;
        cursor: pointer;
      }

      img:hover {
        -moz-transform: scale(1.1);
        -webkit-transform: scale(1.1);
        transform: scale(1.1);
      }

      &__client {
        margin-right: 25px;

        img {
          border-radius: 50%;
          background-color: #fff;
          border: 12px solid black;
          padding: 2rem;
          cursor: pointer;
        }
      }
    }
  }
}
</style>