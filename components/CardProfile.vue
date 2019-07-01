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
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['image_url', 'name']
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
      margin-bottom: 80px;
      &::after{
        position: absolute;
        width: 110%;
        content:"";
        bottom: -20px;
        border-bottom: 4px solid #000;
      }
    }
    .wrap-btm {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__icon {
      width: 160px;
      height: 160px;
      border-radius: 50%;
    }
    &__text {
      display: flex;
      justify-content: center;
      align-items: left;
      align-self: flex-start;
      flex-direction: column;
      text-align: left;
      margin-left: 20px;
      width: 60%;
    }
    &__name {
      font-size: 30px;
      font-weight: 600;
      margin-bottom: 20px;
    }
    &__description {
      font-size: 10px;
    }
  }
</style>
