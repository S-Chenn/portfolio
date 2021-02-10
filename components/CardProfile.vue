<template>
  <div class="profile">
    <h2 class="profile__title">
      Profile
    </h2>
    <p class="profile__ruby">
      プロフィール
    </p>
    <div class="wrap-btm">
      <img src="@/assets/images/adam.jpg" alt="" class="profile__icon">
      <div class="profile__text">
        <h3 class="profile__name">
          {{ name }}
        </h3>
        <slot />
        <div class="twitter-icon">
          <a href="https://twitter.com/SChen90239869" target="_blank" class="twitter-link">
            <font-awesome-icon :icon="['fab', 'twitter']" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {

  props: {
    imageUrl: {
      type: String,
      default: ''
    },
    name: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss" scoped>
  .profile {
    max-width: 600px;
    padding: 10px 20px 20px 20px;
    margin: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &__title {
      font-size: 36px;
      font-weight: 600;
      margin-bottom: 8px;
    }
    &__ruby {
      position: relative;
      font-size: 12px;
      color: #ABABAB;
      margin-bottom: 52px;
      &::after{
        position: absolute;
        width: 110%;
        left: 0;
        content:"";
        bottom: -20px;
        border-bottom: 4px solid #000;
      }
    }
    .wrap-btm {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    &__icon {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      flex-shrink: 0;
      margin-bottom: 32px;
    }
    &__text {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      text-align: left;
      width: 100%;
    }
    &__name {
      font-size: 30px;
      font-weight: 600;
      margin-bottom: 20px;
      text-align: center;
    }
    &__description {
      font-size: 10px;
    }
    .twitter-link {
      text-align: left;
      height: 50px;
      width: 50px;
      margin: 0 auto 0 0;
    }
    .twitter-icon {
      // color: #1DA1F2;
      // padding: 8px;
      // font-size: 48px;
      // height: 50px;
      // width: 50px;
      // display: inline-block;
    }
  }
@include pc() {
  .profile {
    .wrap-btm {
      flex-direction: row;
    }
    &__icon {
      margin: 0;
    }
    &__ruby {
      margin-bottom: 80px;
    }
    &__text {
      align-items: left;
      align-self: flex-start;
      margin-left: 20px;
      width: 60%;
    }
    &__name {
      text-align: left;
      align-self: flex-start;
    }
  }
}
</style>
