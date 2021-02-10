<template>
  <div>
    <div class="hamburger-menu" @click="drawerOn = !drawerOn" />
    <div
      :class="{ jsDrawerMask: drawerOn }"
      @click="drawerOn = !drawerOn"
    />
    <ex-header class="header" :class="{ jsDrawerOpen: drawerOn }" @drawer-close="drawerClose()" />
    <nuxt />
    <ExFooter class="footer" :class="{ jsDrawerOpen: drawerOn }" />
  </div>
</template>

<script>
import ExHeader from '@/components/ExHeader.vue'
import ExFooter from '@/components/ExFooter.vue'
export default {
  components: {
    ExHeader,
    ExFooter
  },
  data() {
    return {
      drawerOn: false
    }
  },
  methods: {
    drawerClose() {
      this.drawerOn = false
    }
  }
}
</script>
<style lang="scss" scoped>
.header {
  transform: translateX(-100%);
  transition: .3s all;
}
.footer {
  transform: translateX(-100%);
  transition: .3s all;
}
.jsDrawerOpen {
  transform: translateX(0);
}
.hamburger-menu {
  position: fixed;
  z-index: 10;
  top: 16px;
  left: 16px;
  width: 32px;
  height: 32px;
  border-top: 4px solid rgba($color: #222, $alpha: 0.9);
  border-bottom: 4px solid rgba($color: #222, $alpha: 0.9);
  &::before{
    position: absolute;
    content: "";
    height: 10px;
    width: 100%;
    border-bottom: 4px solid rgba($color: #222, $alpha: 0.9);
  }
}
.jsDrawerMask {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  opacity: 0.6;
  background-color: #000;
  z-index: 1000;
}
@include pc (){
  .header {
    transform: none;
    transition: none;
  }
  .footer {
    transform: none;
    transition: none;
  }
  .hamburger-menu {
    display: none;
  }
  .jsDrawerMask{
    display: none;
  }
}
</style>
