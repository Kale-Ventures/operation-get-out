<template lang="pug">
.bg-white
  b-row
    b-col.image(
      cols="12"
      md="5"
      lg="4"
      style="background-image: url('https://picsum.photos/seed/srgj/400')"
    )

    b-col(
      cols="12"
      md="7"
      lg="8"
    )
      .px-4.py-4
        h5.date September 24-25, 2022
        h4 Get Out Girl Surf &amp; Paddle Jam Weekend
        .mb-4
          p
            em.font-weight-medium An all-female weekend sharing #bluemindsisterhood! Wakesurf Saturday, Paddle Jam Sunday and weekend after party with food, DJ Coy, Boss Jaguar Surf Band, silent and live auctions with family and friends!
          p Camaraderie, inspiration, and empowerment with amazing like-minded women paddling in memory and honor of Travis County first responders Kristin McLain &amp; Jessica Hollis. All proceeds provide nature and water events, experiences and equipment for front-line workers, military, nurses, surviving family and agencies through Operation Get Out, a 501c3 nonprofit.

        b-row(
          align-h="between"
        )
          b-col(
            cols="12"
            md="auto"
          )
            p(
              style="font-size: 18px;"
            )
              strong.text-uppercase Location:&nbsp;
              | Lake Austin, TX
          b-col(
            cols="12"
            md="auto"
          )
            b-btn Register

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
  min-height: 400px;
  background-size: cover;
  background-position: center;
}
</style>
