<template>
  <section class="hero">
    <no-ssr>
      <carousel
        class="carousel"
        :autoplay-hover-pause="true"
        :per-page="1"
        :autoplay="true"
        :loop="true"
        :autoplay-timeout="5000"
        :speed="1200"
        :navigation-enabled="false"
        :pagination-size="10"
        :pagination-padding="0"
        pagination-active-color="rgba(255, 255, 255, 0.7)"
        pagination-color="transparent"
      >
        <slide><img src="@/assets/images/hero-1.jpg" class="hero__img hero__img-1" alt="hero-1"></slide>
        <slide><img src="@/assets/images/hero-2.jpg" class="hero__img hero__img-2" alt="hero-2"></slide>
        <slide><img src="@/assets/images/hero-3.jpg" class="hero__img hero__img-3" alt="hero-3"></slide>
        <slide><img src="@/assets/images/hero-4.jpg" class="hero__img hero__img-4" alt="hero-4"></slide>
        <slide><img src="@/assets/images/hero-5.jpg" class="hero__img hero__img-5" alt="hero-5"></slide>
      </carousel>
    </no-ssr>
    <div class="heading-wrap">
      <h1 class="heading">
        Welcome to my Portfolio Site
      </h1>
      <div class="dots" />
    </div>
  </section>
</template>

<script>
import Carousel from 'vue-carousel/src/Carousel.vue'
import Slide from 'vue-carousel/src/Slide.vue'
export default {
  components: {
    Carousel,
    Slide
  }
}
</script>

<style lang="scss" scoped>
.VueCarousel {
  position: relative;
}
.VueCarousel-slide {
  background: #36393F;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid #fff;
  box-sizing: border-box;
}
/deep/ .VueCarousel-dot {
  padding: 5%;
  background-color: transparent;
  border: 4px solid rgba(255, 255, 255, 0.7);
  margin: 2%;
}

/deep/ .VueCarousel-dot-container {
  width: 100%;
}

/deep/ .VueCarousel-pagination {
  z-index: 100;
  position: absolute;
  bottom: 10%;
}
 .hero {
   background-color: #36393F;
   position: relative;
   width: 100%;
   .heading-wrap {
     background-color: rgba(0, 0, 0, 0.3);
     position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      .heading {
        font-size: 1.4em;
        color: rgba(255, 255, 255, 0.7);
        text-align: center;
        padding: 0 16px;
      }
   }

   &__img {
     width: 100%;
   }
 }

 @include pc(){
   .hero {
     .heading-wrap {
       .heading {
         font-size: 60px;
         line-height: 1.2;
         padding: auto;
       }
     }
   }
 }
</style>
