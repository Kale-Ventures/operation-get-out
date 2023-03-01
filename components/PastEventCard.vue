<template lang="pug">
  container
    .mb-4
    b-row.px-4.px-md-5.pt-4.bg-white
      b-col(
        cols="12"
      )
        h4 Event Name Excepteur Sint Occaecat Cupidatat
        p.mb-4 Event recap or summary lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur.
        p(
          style="font-size: 18px;"
        )
          strong.text-uppercase.text-secondary Dates:&nbsp;
          | February 16-18, 2023
        p(
          style="font-size: 18px;"
        )
          strong.text-uppercase.text-secondary Location:&nbsp;
          | Chattanooga, TN

    b-row.px-4.px-md-5.pb-5.bg-white(
    )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )
      b-col(
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          src="/images/blank_image.jpg"
        )

    b-row.px-4.px-md-5.bg-primary
      b-col(
        cols="12"
      )
        h5.text-white.pt-2 See the full image gallery &gt;

</template>

<script>
export default {
  name: 'EventCard',
  props: {
    event: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
a {
  text-transform: uppercase;
  font-size: 14px;
  color: $secondary;
  font-weight: 600;
}

.image {
  min-height: 120px;
  min-width: 180px;
  margin-top: 20px;
}

::v-deep em {
  font-weight: 500;
  color: $tertiary;
}
</style>
