<template>
  <section id="profile" class="profile section">
    <div class="container">
      <CardProfile class="profile__card" :image_url="src" name="S-Chen">
        <p class="introduction">
          フロントエンドエンジニアをやっております。John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe
        </p>
      </CardProfile>
      <div class="profile__timeline">
        <a class="twitter-timeline" href="https://twitter.com/SChen90239869?ref_src=twsrc%5Etfw">Tweets by SChen90239869</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8" />
      </div>
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
  .profile {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &__card {
      margin-bottom: 40px;
    }
    .introduction {
      font-size: 10px;
      line-height: 2.0;
    }
  }

@include pc() {
  .profile{
    &__card {
      margin-bottom: 80px;
    }
  }
}
</style>
