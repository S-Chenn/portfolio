<template>
  <section class="hero">
    <no-ssr>
      <carousel
        class="carousel"
        :autoplay-hover-pause="true"
        :per-page="1"
        :autoplay="true"
        :loop="true"
        :pagination-padding="20"
        :autoplay-timeout="5000"
        :speed="1200"
        :navigation-enabled="true"
        :pagination-size="20"
        :pagination-color="DFE0E1"
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
.VueCarousel-slide {
  background: #36393F;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid #fff;
  box-sizing: border-box;
}
 .hero {
   background-color: #36393F;
   position: relative;
   width: 100%;
   .heading-wrap {
      position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      background-color: rgba(0, 0 ,0, .3);
      display: flex;
      justify-content: center;
      align-items: center;
      .heading {
        font-size: 48px;
        color: #ffffff;
        text-align: center;
        padding: 20%;
      }
   }
   .carousel {
   }

   &__img {
     width: 100%;
   }
 }
</style>
