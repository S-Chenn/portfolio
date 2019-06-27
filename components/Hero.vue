<template>
  <section class="hero">
    <no-ssr>
      <slickref="slick" :is="slickComp" :options="slickOptions" class="slick">
        <div><img src="@assets/images/hero-1.png" alt="hero-1"></div>
        <div><img src="@assets/images/hero-2.png" alt="hero-2"></div>
        <div><img src="@assets/images/hero-3.png" alt="hero-3"></div>
        <div><img src="@assets/images/hero-4.png" alt="hero-4"></div>
        <div><img src="@assets/images/hero-5.png" alt="hero-5"></div>
      </slickref="slick">
    </no-ssr>
  </section>
</template>

<script>
import Slick from 'vue-slick'
import '~/node_modules/slick-carousel/slick/slick.css'
export default {
  components: { Slick },

  data() {
    return {
      slickOptions: {
        slidesToShow: 3
        // Any other options that can be got from plugin documentation
      }
    }
  },
  methods: {
    next() {
      this.$refs.slick.next()
    },
    prev() {
      this.$refs.slick.prev()
    },
    reInit() {
      // Helpful if you have to deal with v-for to update dynamic lists
      this.$nextTick(() => {
        this.$refs.slick.reSlick()
      })
    }
  }
}
</script>

<style lang="scss" scoped>
 .hero {
   width: 1000px;
   height: 500px;
 }
</style>
