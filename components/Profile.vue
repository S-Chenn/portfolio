<template>
  <section id="profile" class="profile section">
    <div class="container">
      <Heading class="skills__heading" title="Profile" ruby="プロフィール" />
      <CardProfile class="profile__card" :image_url="src" name="S-Chen">
        <p class="introduction">
          フロントエンドエンジニアをやっております。John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe John Doe
        </p>
      </CardProfile>
      <div class="profile__timeline">
        <a class="twitter-timeline" href="https://twitter.com/SChen90239869?ref_src=twsrc%5Etfw">Tweets by SChen90239869</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8" />
      </div>
      <Btn class="profile__btn" text="詳細を見る" url="https://www.resume.id/s_chen" />
    </div>
  </section>
</template>

<script>
import Heading from '@/components/Heading.vue'
import CardProfile from '@/components/CardProfile.vue'
import Btn from '@/components/Btn.vue'
import src from '~/assets/images/profile-icon.jpg'
export default {
  components: {
    Heading,
    CardProfile,
    Btn
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
      margin-bottom: vw(40);
    }

    &__btn {
      margin: 0 auto;
      width: 50%;
    }
    .introduction {
      font-size: vw(32);
      line-height: 2.0;
    }

  &__timeline {
    margin-bottom: vw(40);
  }

  }

@include pc() {
  .profile{

    width: 100%;
    &__card {
      @include margin(0, 0, 80, 0);
    }

    &__btn {
    }

    &__timeline {
    @include margin(0, 0, 80, 0);
  }

  .introduction {
    @include fz(30);
  }
  }
}
</style>
