<template lang="pug">
div
  .mb-4
  b-row.px-4.px-md-5.pt-4.bg-white
    b-col(
      cols="12"
    )
      h4 {{ event.title }}
      nuxt-content.mb-4(:document="event")
      p(
        style="font-size: 18px;"
      )
        strong.text-uppercase.text-secondary Dates:&nbsp;
        span(
          v-if="event.dateStart !== event.dateEnd"
        ) {{ $dayjs(event.dateStart).add(1, 'day').format("MMMM D") }} - {{ $dayjs(event.dateEnd).add(1, 'day').format("D, YYYY") }}
        span(
          v-else
        ) {{ $dayjs(event.dateStart).add(1, 'day').format("MMMM D, YYYY") }}
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
      b-img-lazy.upper-image.clickable(
        @click.native="isGalleryOpen = true; slide = index"
        fluid-grow
        :src="image"
      )

  b-row.px-4.px-md-5.bg-primary(
    v-if='event.imageGalleryLink'
  )
    b-col.py-2(
      cols="12"
    )
      a.link-reset.text-white(
        :href='event.imageGalleryLink'
      )
        strong See the full image gallery
        b-img-lazy.pl-3.pb-1(
          src="/images/past-events/gt.svg"
        )

  b-modal(
    v-model="isGalleryOpen"
    hide-footer
    hide-header
    centered
    static
    size='lg'
  )
    b-container
      b-row
        b-col
          h4.mb-3 {{ event.title }}

      b-row
        b-col
          b-carousel(
            ref="carousel1"
            :interval="4000"
            v-model='slide'
          )
            b-carousel-slide.carousel-img(
              v-for="(image, index) in event.images"
              :key="index"
              :img-src="image"
            )

      b-row
        b-col(
          cols="6"
        )
          .d-flex.justify-content-start
            .button.mt-3.mb-2(
              @click="previousSlide"
            )
              b-img-lazy(
                src="/images/past-events/prev_arrow.svg"
              )
              b-img-lazy.pl-3(
                src="/images/past-events/PREVIOUS.svg"
              )
        b-col(
          cols="6"
        )
          .d-flex.justify-content-end
            .button.mt-3.mb-2(
              @click="nextSlide"
            )
              b-img-lazy.pr-3(
                src="/images/past-events/NEXT.svg"
              )
              b-img-lazy(
                src="/images/past-events/next_arrow.svg"
              )

      .strip
        .button(
          v-for="(image, index) in event.images"
          :key="index"
          @click="selectSlide(index)"
        )
          b-img-lazy.image(
            fluid
            :src="image"
          )

      .text-center.mt-4(
        v-if='event.imageGalleryLink'
      )
        a.text-primary(
          :href="event.imageGalleryLink"
          style="text-decoration: none;"
        )
          strong See The Full Image Gallery
          b-img-lazy.pl-3.pb-1(
            src="/images/past-events/vector.svg"
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
      isGalleryOpen: false,
      slide: 0
    }
  },
  methods: {
    selectSlide (index) {
      this.$refs.carousel1.setSlide(index)
    },
    previousSlide () {
      this.$refs.carousel1.prev()
    },
    nextSlide () {
      this.$refs.carousel1.next()
    }
  }
}
</script>

<style lang="scss" scoped>

.image {
  margin-top: 10px;
  object-fit: cover;
  height: 60px;
  width: 90px;
  margin-right: 3px;
}

.upper-image {
  margin-bottom: 32px;
  object-fit: cover;
  height: 200px;
}

.carousel-img {
  height: 520px;
}

.button {
  cursor: pointer;
  display: inline-block;
  background-color: white;
  border: none;
  letter-spacing: 1.05px;
  color: white;
}

</style>
