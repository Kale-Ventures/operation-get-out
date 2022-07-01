<template lang="pug">
.bg-white.mb-4.event-card
  b-row
    b-col(
      cols="12"
      md="5"
      lg="4"
    )
      .image(
        :style="`background-image: url('/images/${event.image}.jpg')`"
      )

    b-col(
      cols="12"
      md="7"
      lg="8"
    )
      .px-4.py-4.d-flex.flex-column.fill-height
        h5.date {{ event.date }}
        h4 {{ event.title }}
        .mb-4
          div(
            v-html="$md.render(event.body)"
          )
        b-row.mt-auto(
          align-h="between"
        )
          b-col(
            cols="12"
            md="auto"
          )
            p(
              style="font-size: 18px;"
            )
              strong.text-uppercase.text-primary Location:&nbsp;
              | {{ event.location }}
          b-col(
            cols="12"
            md="auto"
          )
            b-btn(
              :href='event.url'
            ) {{ event.buttonText }}

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
  height: 100%;
  min-height: 400px;
  background-size: cover;
  background-position: center;
}

::v-deep em {
  font-weight: 500;
  color: $tertiary;
}
</style>
