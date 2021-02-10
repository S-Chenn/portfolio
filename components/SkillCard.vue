<template>
  <div class="card">
    <div class="skill">
      <figure class="skill__icon">
        <slot />
      </figure>
      <h3 class="skill__title">
        {{ title }}
      </h3>
      <p class="skill__description">
        {{ description }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    description: {
      type: String,
      default: ''
    } }
}
</script>
<style lang="scss">
.card {
  border-radius: 12px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, .12);
  overflow: hidden;
}
.skill {
  text-align: center;
  color: #fff;
  background: linear-gradient(to top right, #000, #2d033a);
  padding: 24px;
  height: 100%;
  &__icon {
    margin-bottom: 32px;
  }
  &__title {
    margin-bottom: 16px;
  }
  &__description {
    font-size: 13px;
    color: rgba(255, 255, 255, .6);
    line-height: 1.8;
  }
}
</style>
