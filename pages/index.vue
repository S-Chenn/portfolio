<template>
  <div>
    <Hero />
    <Profile />
    <Skills />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
import Profile from '@/components/Profile.vue'
import Skills from '@/components/Skills.vue'
export default {
  components: {
    Hero,
    Profile,
    Skills
  }
}
</script>

<style lang="scss">

</style>
