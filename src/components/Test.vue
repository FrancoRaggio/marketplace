<template>
  <div>
    Realizar aca el diseño
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Test',
  data() {
    return {
      products: [],
    }
  },
  async mounted() {
    const { data } = await axios.get('https://api.turismocity.com/cuarentena/products');
    this.products = data;
  }
}
</script>

<style scoped>
</style>
