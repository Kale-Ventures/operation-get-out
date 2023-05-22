<template lang="pug">
  main
    section.hero
      b-container
        b-row.hero-row.px-4.px-md-0.pt-2.pt-md-5(
          align-v="center"
        )
          b-col.pt-5(
            cols="auto"
          )
            h1.text-white.title(
            ) Upcoming Events

    section.banner.px-3(
      style="background-color: #eaf7ff"
    )
      b-container
        b-row.bg-tertiary.text-white.py-4.px-4.px-md-5.text-row(
          align-v="center"
        )
          b-col(
            cols="12"
          )
            p Our events bring the community together to experience nature and discover wellness. Paddleboarding to cycling, yoga to wakesurfing, find an event and register to Get Out with us and experience wellness in the great outdoors.

    section.events
      b-container
        b-row.pt-4.pt-md-5
          b-col
            UpcomingEventCard(
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
      .where({ dateStart: { $gt: new Date() } })
      .sortBy('dateStart', 'asc')
      .fetch()

    return {
      events
    }
  }
}
</script>

<style lang="scss" scoped>

section.hero {
  background-image: url('/images/upcoming-events/hero.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  z-index: 1;
}

.hero-row {
  min-height: 345px;
}

section.banner {
  margin-top: -50px;
  .text-row {
    position: relative;
    z-index: 10;
  }
}

section.events {
  background-color: #eaf7ff;
  padding-bottom: 40px;
}

section.to-past-events {
  background-color: #eaf7ff;
  padding-top: 10px;
  padding-bottom: 60px;
}

.title {
  padding: 0 20px;
  background-color: $tertiary;

  @include media-breakpoint-down(sm) {
    font-size: 50px;
  }
}

</style>
