<template lang="pug">
  footer
    b-container(
      fluid="xxl"
    )
      b-row
        b-col
          p.text-right.mb-0 Copyright {{new Date().getFullYear()}} &copy; All Rights Reserved. Operation Get Out.
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss">
footer {
  padding-top: 20px;
  padding-bottom: 20px;
}
</style>
