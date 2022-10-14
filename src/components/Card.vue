<template>
    <div class="col">
        <div class="card">
            <img :src="link.image" class="card-img-top" alt="">
            <div class="card-img-overlay d-flex flex-column justify-content-end text-white card-info-text">
                <h2 class="card-title card-text-size card-text-desktop" v-if="link.title !== ''">{{link.title}}</h2>
                <p class="card-text card-text-size card-subtitle-desktop" v-if="link.subtitle !== ''">{{link.subtitle}}</p>
                <p class="card-text card-text-size card-text-desktop" v-if="link.price !== 0">${{link.price}}</p>
            </div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'Card',
  data() {
    return {
    }
  },
  props: {
        link: []
    }
}
</script>

<style scoped>
    .card-info-text {
        text-shadow: 0.1px 1.5px 0 rgb(0 0 0 / 31%);
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
    }
    @media (max-width: 768px) { 
        .card-text-size {
            font-size: 15px;
            line-height: 15px;
        }
    }
    @media (min-width: 768px) { 
        .card-text-desktop {
            font-size: 22px;
            line-height: 23px;
        }
        .card-subtitle-desktop {
            font-size: 14px;
            line-height: 16px;
        }
    }   
</style>
