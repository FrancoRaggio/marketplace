<template>
  <div class="header">
    <div class="info-seccion">
      <div class="col-12 col-md-6">
        <h1 class="item-title">{{item.title}}</h1>
        <p class="item-subtitle">{{item.subtitle}}</p>
      </div>
      <div class="img-seccion">
        <img  :src="item.image" alt="" width="215px" height="76px">
      </div>
    </div>
    <div class="row row-cols-md-4 row-cols-2 row-cols-md-1 g-2">
      <Card v-for="(link, index) in item.links" :key="index" :link="link"/>
    </div>

    <div class="d-flex justify-content-center my-5">
      <a class="item-button" :href="item.home">Ver más opciones en <strong>{{item.name}}</strong></a>
    </div>
  </div>
</template>

<script>
import Card from '../components/Card.vue'

export default {
  name: 'Seccion',
  components: {
    Card
  },
  props: {
    item: []
  }
}
</script>

<style scoped>
@media (max-width: 768px) { 
  .info-seccion {
    text-align: center;
  }
  .img-seccion {
    margin-bottom: 1.5rem;
  }
}
  .header {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
  }
  .item-title {
    font-size: 23px;
    line-height: 27px;
    color: #1D4D8B;
  }
  .item-subtitle {
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;

    color: #1D4D8B;
  }

  .item-button {
    font-weight: 400;
    font-size: 20px;
    line-height: 23px;
    text-align: center;
    background: #4285F4;
    border-radius: 50px;
    color: #FFFFFF;
    border: 1rem solid transparent;
    text-decoration: none;
  }
</style>
