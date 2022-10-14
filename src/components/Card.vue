<template>
    <div class="col">
        <div class="card">
            <img :src="link.image" class="card-img-top" alt="">
            <div class="card-img-overlay d-flex flex-column justify-content-end">
                <h5 class="card-title card-title" :class="isMobile ? 'card-title-mobile' : 'card-title-desktop' " v-if="link.title !== ''">{{link.title}}</h5>
                <p class="card-text card-subtitle" :class="isMobile ? 'card-subtitle-mobile' : 'card-subtitle-desktop' " v-if="link.subtitle !== ''">{{link.subtitle}}</p>
                <p class="card-text card-price" :class="isMobile ? 'card-price-mobile' : 'card-price-desktop' " v-if="link.price !== 0">${{link.price}}</p>
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
        link: [],
        isMobile: Boolean
    }
}
</script>

<style scoped>
    .card-title-mobile {
        font-size: 16px;
        line-height: 16px;
    }
    .card-title-desktop {
        font-size: 22px;
        line-height: 23px;
    }
    .card-title {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
        color: #FFFFFF;
        text-shadow: 0px 1px 3px black;
    }
    .card-subtitle-mobile {
        font-size: 10px;
        line-height: 15px;
    }
    .card-subtitle-desktop {
        font-size: 14px;
        line-height: 16px;
    }
    .card-subtitle {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 500;
        color: #FFFFFF;
        text-shadow: 0px 1px 3px black;
    }
    .card-price-mobile {
        font-size: 16px;
        line-height: 16px;
    }
    .card-price-desktop {
        font-size: 22px;
        line-height: 22px;
    }
    .card-price {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
        color: #FFFFFF;
        text-shadow: 0px 1px 3px black;
    }
</style>
