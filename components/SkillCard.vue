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
  props: ['title', 'description']
}
</script>
<style lang="scss">

</style>
