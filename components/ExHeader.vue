<template>
  <header class="header">
    <div class="header__logo">
      <nuxt-link v-scroll-to="{el:'#top', offset: hedderOffset}" to="/" class="header__logo-link" @click.native="close">
        Potofolio
      </nuxt-link>
    </div>
    <nav class="header__nav">
      <ul class="header__nav-list">
        <li class="header__nav-item">
          <nuxt-link v-scroll-to="'#profile'" to="/#profile" class="header__nav-link" @click.native="close">
            Profile
          </nuxt-link>
        </li>
        <li class="header__nav-item">
          <nuxt-link v-scroll-to="'#skills'" to="/#skills" class="header__nav-link" @click.native="close">
            Skills
          </nuxt-link>
        </li>
        <li class="header__nav-item">
          <nuxt-link to="/contact" class="header__nav-link" @click.native="close">
            Contact
          </nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {

  data() {
    return {
      hedderOffset: {
        type: Number,
        default: 0
      }
    }
  },
  mounted() {
    this.close()
  },
  methods: {
    close() {
      this.$nuxt.$emit('close')
    },
    calcHeadderOffset() {
    }
  }
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
    height: initial;
    background-color: rgba(0, 0, 54, 0.80);
    flex-direction: row;
    color: #fff;
    align-items: center;
    @include padding(32, 60);
    transform: none;
      &__logo {
      margin: 0;
      @include fz(40);
    }

    &__nav-list {
      flex-direction: row;
    }
    &__nav-item {
      padding: 0;
      @include margin(0, 20);
      @include fz(32);
      line-height: 1;
      height: initial;

      &::before {
        position: absolute;
        content: "";
        right: 50%;
        bottom: -4px;
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
        bottom: -4px;
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
    }
  }
</style>
