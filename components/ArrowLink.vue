<template lang="pug">
  nuxt-link(
    v-bind="$attrs"
  )
    slot
    | &nbsp;&gt;
</template>

<script>
// import ArrowRight from '~/assets/svgs/arrow-nav-right.svg?inline'

export default {
  name: 'ArrowLink'
  // components: {
  //   ArrowRight
  // }
}
</script>

<style lang="scss" scoped>
a {
  text-transform: uppercase;
  font-size: 14px;
  color: $secondary;
  font-weight: 600;
}
</style>
