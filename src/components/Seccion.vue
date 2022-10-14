<template>
  <div :class="isMobile ? '' : ''">
    <div :class="isMobile ? 'text-center' : 'd-inline-flex'">
      <div :class="isMobile ? 'col-12' : 'col-6'">
        <h1 class="item-title">{{item.title}}</h1>
        <p class="item-subtitle">{{item.subtitle}}</p>
      </div>
      <div :class="isMobile ? 'mb-4' : 'ms-auto'">
        <img  :src="item.image" alt="" width="215px" height="76px">
      </div>
    </div>
    <div class="row row-cols-md-4 g-2" :class="isMobile ? 'row-cols-2' : 'row-cols-1'">
      <Card v-for="(link, index) in item.links" :key="index" :link="link" :isMobile="isMobile"/>
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
    item: [],
    isMobile: Boolean
  }
}
</script>

<style scoped>
  .item-title {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
    font-size: 23px;
    line-height: 27px;
    color: #1D4D8B;
  }
  .item-subtitle {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;

    color: #1D4D8B;
  }

  .item-button {
    font-family: 'Roboto';
    font-style: normal;
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
