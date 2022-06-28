<template lang="pug">
.testimonial
  p.quote Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqu.
  p.attribution @Ralph_Keller
  p.title Job Title

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

.quote {
  color: #A1AEB7;
  font-size: 18px;
}

.attribution {
  margin-bottom: 0;
}

.title {
  color: #A1AEB7;
  font-size: 14px;
  margin-bottom: 0;
}
</style>
