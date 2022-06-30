<template lang="pug">
b-card.text-center.team-member.fill-height(
  border-variant="light"
  :img-src="`/images/headshots/${member.name}.jpg`"
)
  h4.text-tertiary {{ member.name }}

</template>

<script>
export default {
  name: 'TestimonialCard',
  props: {
    member: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.team-member {
  background-color: #eaf7ff;

  h4 {
    font-size: 24px;
  }
}
</style>
