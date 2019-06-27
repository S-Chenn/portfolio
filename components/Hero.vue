<template>
  <section class="hero">
    <no-ssr>

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

</style>
