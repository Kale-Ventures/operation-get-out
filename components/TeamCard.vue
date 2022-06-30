<template lang="pug">
b-card.text-center.team-member.fill-height(
  border-variant="light"
  :img-src="`/images/headshots/${member.name}.jpg`"
)
  h4.text-tertiary {{ member.name }}
  a(
    @click='isBioOpen = true'
  )
    | Read More
    ArrowRight.ml-2

  b-modal(
    :title='member.name'
    v-model='isBioOpen'
    hide-footer
    static
  )
    p {{ member.bio }}

</template>

<script>
import ArrowRight from '~/assets/svgs/arrow-nav-right.svg?inline'

export default {
  name: 'TestimonialCard',
  components: {
    ArrowRight
  },
  props: {
    member: {
      type: Object,
      required: true
    }
  },
  data () {
    return {
      isBioOpen: null
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

a {
  text-transform: uppercase;
  font-size: 14px;
  color: $secondary !important;
  font-weight: 600;

  cursor: pointer;
}
</style>
