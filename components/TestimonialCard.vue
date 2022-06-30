<template lang="pug">
.testimonial.mb-4.mb-md-0.fill-height
  b-img.mb-5(
    src="/images/quote.svg"
    width="30"
  )
  p.quote {{ testimonial.quote }}
  p.attribution {{ testimonial.attribution }}
  p.title(v-if="testimonial.title") {{ testimonial.title}}

</template>

<script>
export default {
  name: 'TestimonialCard',
  props: {
    testimonial: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.testimonial {
  text-align: center;
  background-color: #fff;
  padding: 60px 30px;
}

img {
  transform: rotate(180deg);
}

.quote {
  font-size: 18px;
}

.attribution {
  margin-bottom: 0;
  font-size: 22px;
  color: $tertiary;
}

.title {
  color: #A1AEB7;
  font-size: 14px;
  margin-bottom: 0;
}
</style>
