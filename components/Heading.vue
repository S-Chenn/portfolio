<template>
  <div class="heading">
    <h2 class="heading__title">
      {{ title }}
    </h2>
    <p class="heading__ruby">
      {{ ruby }}
    </p>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    ruby: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss" scoped>
.heading {
  padding: vw(10) vw(20) vw(20) vw(20);
  margin: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  @include pc(){
  padding: 10px 20px 20px 20px;
  }

  &__title {
    font-size: vw(48);
    font-weight: 600;
    margin-bottom: 8px;
    text-align: center;
    line-height: 1.3;

    @include pc(){
      @include fz(60);
    }

  }
  &__ruby {
    position: relative;
    font-size: vw(16);
    color: #ABABAB;
    margin-bottom: 40px;
    text-align: center;

  @include pc(){
    @include fz(16);
  }

  }
}
/deep/ .heading__ruby::after {
      position: absolute;
      left: 0;
      width: 110%;
      content:"";
      bottom: -20px;
      border-bottom: 4px solid #000;
}
@include pc() {
.heading {
  &__ruby {
    margin-bottom: 80px;
  }
}
}
</style>
