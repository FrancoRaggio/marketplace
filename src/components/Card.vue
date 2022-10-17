<template>
    <div class="position-relative">
        <div class="card border-0">
            <img :src="link.image" class="img-fluid " alt="">
            <div class="card-img-overlay d-flex flex-column justify-content-end text-white card-info-text text-start">
                <h2 class="card-title card-text-decoration card-text-desktop card-text-mobile" v-if="link.title !== ''">{{link.title}}</h2>
                <p class="card-text card-text-decoration card-subtitle-desktop card-subtitle-mobile mb-2" v-if="link.subtitle !== ''">{{link.subtitle}}</p>
                <p class="card-text card-text-decoration card-text-desktop card-text-mobile mb-0" v-if="link.price !== 0">${{link.price}}</p>
                <div class=" img-gradient position-absolute top-0 start-0 mb-0"></div>
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
    link: {}
  }
}
</script>

<style scoped>
    img {
        border-radius: 16px;
    }
    .card-info-text {
        text-shadow: 0px 1px 0px rgba(0, 0, 0, 0.08);
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
    }
    .card-info-text > .card-text-decoration {
        z-index: 1;
        text-shadow: 0px 1px 0px rgba(0, 0, 0, 0.08);
        margin-right: 10%;
    }
    .img-gradient {
        width: 100%;
        height: 100%;
        background: linear-gradient(180deg,transparent 60%,rgba(0,0,0,.4));
        border-radius: 16px;
    }
    @media (max-width: 768px) { 
        .card-text-mobile {
            font-size: 14px;
            line-height: 13px;
        }
        .card-subtitle-mobile {
            font-size: 8px;
            line-height: 7px;
        }
    }
    @media (min-width: 768px) { 
        .card-text-desktop {
            font-size: 25px;
            line-height: 22px;
        }
        .card-subtitle-desktop {
            font-size: 18px;
            line-height: 16px;
        }
    }   
</style>
