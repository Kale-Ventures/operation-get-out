<template lang="pug">
  container
    .mb-4
    b-row.px-4.px-md-5.pt-4.bg-white
      b-col(
        cols="12"
      )
        h4 {{event.headline}}
        nuxt-content.mb-4(:document="event")
        p(
          style="font-size: 18px;"
        )
          strong.text-uppercase.text-secondary Dates:&nbsp;
          | {{ $dayjs(event.dateStart).format("MMMM D") }} - {{ $dayjs(event.dateEnd).format("D, YYYY") }}
        p(
          style="font-size: 18px;"
        )
          strong.text-uppercase.text-secondary Location:&nbsp;
          | {{event.location}}

    b-row.px-4.px-md-5.pb-5.bg-white
      b-col(
        v-for="(image, index) in event.images"
        :key="index"
        cols="6"
        lg="3"
      )
        b-img-lazy.image(
          fluid
          :src="image"
        )

    b-row.px-4.px-md-5.bg-primary
      b-col(
        cols="12"
      )
        b-btn(
          @click="isGalleryOpen = true"
        ) See the full image gallery &nbsp; &gt;
        b-modal(
          v-model="isGalleryOpen"
          hide-footer
          hide-header
          centered
          static
        )
          b-container
            b-row
              b-col
                h4 Event Name Excepteur Sint Occaecat Cupidatat
            b-row
              b-col
                b-carousel(
                  id="carousel-1"
                  :interval="2000"
                  img-width="1024"
                  img-height="480"
                )
                  b-carousel-slide(
                    img-src="/images/blank_image.jpg"
                  )
                  b-carousel-slide(
                    img-src="/images/bike.jpg"
                  )
                  b-carousel-slide(
                    img-src="/images/donations.jpg"
                  )

</template>

<script>
export default {
  name: 'EventCard',
  props: {
    event: {
      type: Object,
      required: true
    }
  },
  data () {
    return {
      isGalleryOpen: false
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
  margin-top: 10px;
}

::v-deep em {
  font-weight: 500;
  color: $tertiary;
}

</style>
