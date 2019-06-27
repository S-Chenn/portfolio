<template>
  <section class="hero">
    <no-ssr>
      <carousel class="carousel">
        <slide><img src="@/assets/images/hero-1.jpg" alt="hero-1"></slide>
        <slide><img src="@/assets/images/hero-2.jpg" alt="hero-2"></slide>
        <slide><img src="@/assets/images/hero-3.jpg" alt="hero-3"></slide>
        <slide><img src="@/assets/images/hero-4.jpg" alt="hero-4"></slide>
        <slide><img src="@/assets/images/hero-5.jpg" alt="hero-5"></slide>
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
 .hero {
   width: 1000px;
   height: 500px;
 }
</style>
