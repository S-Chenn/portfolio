<template>
  <header class="header">
    <div class="header__logo">
      <nuxt-link v-scroll-to="'#top'" to="/" class="header__logo-link" @click="this.$emit('drawerClose')">
        Potofolio
      </nuxt-link>
    </div>
    <nav class="header__nav">
      <ul class="header__nav-list">
        <li class="header__nav-item">
          <nuxt-link v-scroll-to="'#profile'" to="/" class="header__nav-link" @click="this.$emit('drawerClose')">
            Profile
          </nuxt-link>
        </li>
        <li class="header__nav-item">
          <nuxt-link v-scroll-to="'#skills'" to="/" class="header__nav-link" @click="this.$emit('drawerClose')">
            Skills
          </nuxt-link>
        </li>
        <li class="header__nav-item">
          <nuxt-link to="/contact" class="header__nav-link" @click="this.$emit('drawerClose')">
            Contact
          </nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
}
</script>
<style lang="scss" scoped>
  .header {
    position: fixed;
    z-index: 2000;
    width: 60%;
    height: 60%;
    background-color: #aaaaaa;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    padding: 64px 32px;

    &__logo {
      font-size: 28px;
      margin-bottom: 24px;
    }

    &__nav-list {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
    }
    &__nav-item {
      position: relative;
      margin: 16px 0;
      height: 100%;
      font-size: 20px;
      &::before {
        position: absolute;
        content: "";
        right: 50%;
        bottom: 0;
        width: 0;
        height: 4px;
        background-color: #fff;
        opacity: 0;
        transition: all .5s ease;
      }
      &:hover::before {
        opacity: 1;
        width: 50%;
      }
      &::after {
        position: absolute;
        content: "";
        left: 50%;
        bottom: 0;
        width: 0;
        height: 4px;
        background-color: #fff;
        opacity: 0;
        transition: all .5s ease;
      }
      &:hover::after {
        opacity: 1;
        width: 50%;
      }
    }
    &__nav-link {
      color: #fff;
      text-decoration: none;
    }
    &__logo-link {
      color: #fff;
      text-decoration: none;
    }
  }
  @include pc(){
    .header{
    width: 100%;
    height: 80px;
    background-color: rgba(0, 0, 54, 0.80);
    flex-direction: row;
    color: #fff;
    align-items: center;
    padding: 32px;
    transform: none;
       &__logo {
      margin: 0;
      font-size: 28px;
    }

    &__nav-list {
      flex-direction: row;
    }
    &__nav-item {
      padding: 28px 16px;
      margin: 0 16px;
      font-size: 24px;
    }
    }
  }
</style>
