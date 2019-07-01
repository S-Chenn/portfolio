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
  props: ['title', 'ruby']
}
</script>
<style lang="scss" scoped>
.heading {
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
}
</style>
