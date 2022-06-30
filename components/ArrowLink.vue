<template lang="pug">
  a(
    v-bind="$attrs"
  )
    slot
    ArrowRight.ml-2
</template>

<script>
import ArrowRight from '~/assets/svgs/arrow-nav-right.svg?inline'

export default {
  name: 'ArrowLink',
  components: {
    ArrowRight
  }
}
</script>

<style lang="scss" scoped>
a {
  text-transform: uppercase;
  font-size: 14px;
  color: $secondary !important;
  font-weight: 600;

  cursor: pointer;
}
</style>
