<template>
  <div>
    <a :href="url" class="btn-link"><button class="btn"> {{ text }}</button></a>
  </div>
</template>
<script>
export default {
  props: {
    url: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss" scoped>
  .btn-link {
  }

  .btn {
    cursor: pointer;
    position: relative;
    width: 100%;
    line-height: 3;
    background: linear-gradient(to top right, #000, #2d033a);
    color: #fff;
    font-weight: 600;
    font-size: 3.125vw;
    padding: 0 24vw;
    margin: 0 auto;
    &::after {
      position: absolute;
      content: "▶";
      color: #fff;
      margin-left: 16%;
    }

    &:hover {
      opacity: 0.77;
    }
  }

  @include pc(){
  .btn-link {

  }

  .btn {
    @include fz(28);
    padding: 0;
    line-height: 3;

    &::after {
      margin-left: 84px;
    }
  }
  }
</style>
