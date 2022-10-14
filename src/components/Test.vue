<template>
  <div>
    <Navbar />
      <div class="position-relative">
      <img src="../img/fondo_cuarentena.png" alt="" width="100%" height="223" />
        <h1 class="title-head position-absolute" :class="isMobile ? 'title-head-mobile text-center' : 'title-head-desktop'" >Ofertas para aprovechar desde tu casa</h1>
      </div>
    <Seccion :item="item" v-for="(item, index) in products" :key="index" class="m-2" :isMobile="isMobile"/>
    <Footer :isMobile="isMobile"/>
  </div>
</template>

<script>
import Seccion from '../components/Seccion.vue'
import Footer from '../components/Footer.vue'
import Navbar from '../components/Navbar.vue'
import axios from 'axios';

export default {
  name: 'Test',
  components: {
    Footer,
    Navbar,
    Seccion
  },
  data() {
    return {
      products: []
    }
  },
  computed: {
    isMobile: function () { 
      return !window.matchMedia("(min-width: 764px)").matches
    }
  },
  async mounted() {
    const { data } = await axios.get('https://api.turismocity.com/cuarentena/products');
    this.products = data;
  }
}
</script>

<style scoped>
  /* .title{
    top:50%;
    left: 30%;
    right: 10%;
    transform: translateX(-50%);
  } */
  .title-head {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
  }
  .title-head-desktop {
    width: 100%;
    height: auto;
    font-size: 60px;
    line-height: 65px;

    color: #FFFF;

  }
  .title-head-mobile {
    top:50%;
    left: auto;
    right: auto;
    transform: translateY(-50%);
    font-size: 30px;
    line-height: 35px;
    color: #FFFFFF;
  }
</style>
