<template>
  <div>
    <Navbar/>
      <div class="position-relative header-img">
      <img src="../img/fondo_cuarentena.png" class="w-100" height="100%" alt="" />
        <h1 class="position-absolute top-50 start-50 translate-middle text-center w-100 text-white display-6 fw-bold">Ofertas para aprovechar desde tu casa</h1>
      </div>
    <Seccion :item="item" v-for="(item, index) in products" :key="index" class="m-2 m-md-5" :lastItem="index + 1  >= products.length"/>
    <Footer/>
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
  async mounted() {
    const { data } = await axios.get('https://api.turismocity.com/cuarentena/products');
    this.products = data;
  }
}
</script>

<style scoped>
h1 {
  font-size: 60px;
}
@media (max-width: 768px) { 
  h1 {
    font-size: 30px;
  }
  .header-img {
    height: 162px;
  }
}
</style>
