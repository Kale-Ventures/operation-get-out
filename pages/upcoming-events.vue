<template lang="pug">
  main
    section.hero
      b-container
        b-row.hero-row(
          align-v="center"
        )
          b-col(
            cols="12"
          )
            h1.text-white.pt-5(
            ) Upcoming Events

    section.banner.px-3(
      style="background-color: #eaf7ff"
    )
      b-container
        b-row.bg-tertiary.text-white.py-4.px-5.text-row(
          align-v="center"
        )
          b-col(
            cols="12"
          )
            p Our events bring the community together to experience nature and discover wellness. Paddleboarding to cycling, yoga to wakesurfing, find an event and register to Get Out with us and experience wellness in the great outdoors.

    section.events
      b-container
        b-row
          b-col.text-center
            h2.text-tertiary.mb-5 Upcoming Events

        b-row
          b-col
            EventCard(
              v-for="(event, index) in events"
              :key="index"
              :event="event"
            )

    section.to-past-events
      b-container
        nuxt-link(
          to="/past-events"
          style="text-decoration: none;"
        )
          b-row.bg-primary.py-4.text-white(
            align-v="center"
          )
            b-col(
              cols="12"
              md="6"
              lg="5"
            )
              b-img(
                src="/images/events.jpg"
                fluid
              )
            b-col.mt-3.mt-md-0(
              cols="12"
              md="6"
              lg="7"
            )
              h2.h3 See Past Events
              p See photo galleries and recaps of our past events.

    Connect

</template>

<script>
export default {
  async asyncData ({ $content }) {
    const events = await $content('events')
      .sortBy('dateStart', 'asc')
      .fetch()

    return {
      events
    }
  }
}
</script>

<style lang="scss" scoped>

.hero {
  background-image: url('/images/upcoming-events/kayak_hero.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  z-index: 1;
}

.hero-row {
  min-height: 345px;
}

.banner {
  margin-top: -45px;
  .text-row {
    position: relative;
    z-index: 10;
  }
}

.events {
  background-color: #eaf7ff;
  padding-top: 40px;
  padding-bottom: 40px;
}

.to-past-events {
  background-color: #eaf7ff;
  padding-top: 10px;
  padding-bottom: 60px;
}

</style>
