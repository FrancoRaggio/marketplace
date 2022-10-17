<template>
  <div>
    <div class="info-seccion">
      <div class="col-12 col-md-10 text-md-start">
        <h1 class="item-title fw-bold">{{item.title}}</h1>
        <p class="item-subtitle">{{item.subtitle}}</p>
      </div>
      <div class="img-seccion">
        <img :src="item.image" alt="" class="h-auto">
      </div>
    </div>
    <div class="row row-cols-md-4 row-cols-2 g-2">
      <Card v-for="(link, index) in item.links" :key="index" :link="link"/>
    </div>

    <div class="d-flex justify-content-center my-5">
      <a class="item-button" :href="item.home">Ver más opciones en <strong>{{item.name}}</strong></a>
    </div>
    <hr class="bg-grey" v-if="lastItem !== true">
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
    item: {},
    lastItem: Boolean
  }
}
</script>

<style scoped>
  .info-seccion {
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: space-between;
    color: #1D4D8B;
  }
  .item-title {
    font-size: 23px;
    line-height: 27px;
  }
  .item-subtitle {
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
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
  @media (max-width: 768px) { 
    .info-seccion {
      display: block;
    }
    img {
      width: 215px;
      height: 76px;
    }
    .img-seccion {
      margin-bottom: 1.5rem;
    }
  }
  @media (min-width: 768px) { 
    img {
      width: 100%;
    }
  }
</style>
