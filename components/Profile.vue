<template>
  <section class="profile-section">
    <div class="container">
      <CardProfile image="image_src" name="Chen Zhenyi" desc="うんこぶりぶりぶりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅりゅ" />
    </div>
  </section>
</template>

<script>
import CardProfile from '@/components/CardProfile.vue'
export default {
  components: {
    CardProfile
  },
  data() {
    return {
      image_src: require('@/assets/images/adam.jpg')
    }
  }
}
</script>
<style lang="scss" scoped>
  .profile-section {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 1000px;
  }
</style>
