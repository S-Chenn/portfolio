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
        :autoplay-timeout="1000"
        :speed="1200"
        :navigation-enabled="true"
        :pagination-size="20"
      >
        <slide><img src="@/assets/images/hero-1.jpg" class="hero__img hero__img-1" alt="hero-1"></slide>
        <slide><img src="@/assets/images/hero-2.jpg" class="hero__img hero__img-2" alt="hero-2"></slide>
        <slide><img src="@/assets/images/hero-3.jpg" class="hero__img hero__img-3" alt="hero-3"></slide>
        <slide><img src="@/assets/images/hero-4.jpg" class="hero__img hero__img-4" alt="hero-4"></slide>
        <slide><img src="@/assets/images/hero-5.jpg" class="hero__img hero__img-5" alt="hero-5"></slide>
      </carousel>
    </no-ssr>
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
    background: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid #fff;
  box-sizing: border-box;
}
 .hero {
   width: 100%;

   &__img {
     width: 100%;
   }
 }
</style>
