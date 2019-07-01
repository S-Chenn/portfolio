<template>
  <footer class="footer">
    <nav class="footer-nav">
      <ul class="footer-nav__list">
        <li class="footer-nav__item">
          <nuxt-link class="footer-nav__link" to="">
            Profile
          </nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link class="footer-nav__link" to="">
            Skills
          </nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link class="footer-nav__link" to="">
            Contact
          </nuxt-link>
        </li>
      </ul>
    </nav>
    <small class="footer__copyright">&copy; S-Chen 2019</small>
  </footer>
</template>
<script>
export default {
}
</script>
<style lang="scss" scoped>
.footer {
  position: fixed;
  z-index: 110;
  bottom: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
  padding: 8px 32px;
  background-color: #dddddd;
  height: 40%;
  width: 60%;
  .footer-nav {
    display: flex;
    justify-content: center;
    align-items: center;
    &__list {
      display: flex;
      justify-content: space-evenly;
      align-items: flex-start;
      flex-direction: column;
      padding: -8px;
    }
    &__item {
      padding: 8px;
    }
    &__link {
      font-size: 16px;
      color: #777777;
      text-decoration: none;
    }
  }
  &__copyright {
    color: #999999;
    font-size: 12px;
    align-self: flex-end;
  }
}

@include pc() {
.footer {
  position: initial;
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
  padding: 16px 32px;
  background-color: #FAFAFA;
  .footer-nav {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    &__list {
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      align-items: center;
      padding: -16px;
    }
    &__item {
      padding: 16px;
    }
    &__link {
      font-size: 16px;
      color: #777777;
      text-decoration: none;
    }
  }
  &__copyright {
    color: #999999;
    font-size: 12px;
    align-self: center;
  }
}

.footer-nav__item + .footer-nav__item:before {
  content: "|";
  color: #777777;
  margin: 0 40px;
}
}
</style>
