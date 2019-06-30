<template>
  <section class="profile-section">
    <div class="container">
      <CardProfile :image_url="src" name="Chen Zhenyi">
        <p class="introduction">
          フロントエンドエンジニア(自称)をやっています。前職は無職、部活は帰宅部のエリートニート街道を歩んでおりました。
          南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏南無阿弥陀仏
        </p>
      </CardProfile>
    </div>
  </section>
</template>

<script>
import CardProfile from '@/components/CardProfile.vue'
import src from '~/assets/images/adam.jpg'
export default {
  components: {
    CardProfile
  },
  data() {
    return {
      icon: src
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
    padding: 40px 0;
    .introduction {
      font-size: 10px;
      line-height: 2.0;
    }
  }

@include pc() {
  .profile-section {
    padding: 80px 0;
  }
}
</style>
