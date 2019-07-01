<template>
  <div>
    <ex-header />
    <nuxt />
    <ExFooter />
  </div>
</template>

<script>
import ExHeader from '@/components/ExHeader.vue'
import ExFooter from '@/components/ExFooter.vue'
export default {
  components: {
    ExHeader,
    ExFooter
  }
}
</script>
<style>
</style>
