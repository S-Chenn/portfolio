<template>
  <div>
    <Hero />
    <Profile />
    <Skills />
    <Youtube />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
import Profile from '@/components/Profile.vue'
import Skills from '@/components/Skills.vue'
import Youtube from '@/components/Youtube.vue'
export default {
  components: {
    Hero,
    Profile,
    Skills,
    Youtube
  }
}
</script>

<style lang="scss">
</style>
