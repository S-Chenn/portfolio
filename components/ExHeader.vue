<template>
  <header class="header">
    <div class="header__logo">Portfolio</div>
    <nav class="header__nav">
      <ul class="header__nav-list">
        <li class="header__nav-item">Profile</li>
        <li class="header__nav-item">Skills</li>
        <li class="header__nav-item">Contact</li>
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
    z-index: 1000;
    width: 100%;
    height: 80px;
    background-color: rgba(0, 0, 54, 0.6);
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 32px;

    &__logo {
      font-size: 28px;
    }

    &__nav-list {
      display: flex;
      justify-content: space-evenly;
    }
    &__nav-item {
      position: relative;
      padding: 28px 16px;
      margin: 0 16px;
      height: 100%;
      font-size: 24px;
      &::before {
        position: absolute;
        content: "";
        left: 0;
        bottom: 0;
        width: 100%;
        height: 4px;
        background-color: #fff;
        opacity: 0;
        transition: opacity .5s;
      }
      &:hover::before {
        opacity: 1;
      }
    }
  }
</style>
