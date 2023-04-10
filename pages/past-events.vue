<template lang="pug">
main
  section.hero
    b-container
      b-row.hero-row.px-4.px-md-0.pt-2.pt-md-5(
        align-v="end"
      )
        b-col.pt-5(
          cols="auto"
        )
          h1.text-white.title(
          ) Past Events

  section.events
    b-container
      b-row.pt-4.pt-md-4
        b-col
          PastEventCard(
            v-for="(event, index) in events"
            :key="index"
            :event="event"
          )

  section.to-upcoming-events
    b-container
      nuxt-link(
        to="/upcoming-events"
        style="text-decoration: none;"
      )
        b-row.bg-tertiary.py-4.text-white(
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
            cols="11"
            md="6"
            lg="7"
          )
            h2.h3 See Our Upcoming Events
            p Our events bring the community together to experience nature and discover wellness. Find an event and register to Get Out with us.

  Connect

</template>

<script>
export default {
  async asyncData ({ $content }) {
    const events = await $content('events')
      .where({ dateEnd: { $lt: new Date().toISOString() } })
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
  background-image: url('/images/past-events/hero.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding-bottom: 40px;
}

.hero-row {
  min-height: 345px;
}

section.events {
  background-color: #eaf7ff;
  padding-bottom: 40px;
}

section.to-upcoming-events {
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
