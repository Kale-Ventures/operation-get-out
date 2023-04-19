<template lang="pug">
main
  section.hero.bg-tertiary
    b-container
      b-row.hero-row(
        align-v="center"
      )
        b-col(
          cols="12"
          md="9"
          lg="8"
        )
          h1.text-white {{ page.headerHeadline }}
          p.text-white {{ page.headerSubHeadline }}

  section.banner
    b-container
      b-row.bg-secondary.py-3.text-white(
        align-v="center"
      )
        b-col(
          cols="12"
          md="6"
          lg="5"
        )
          b-img(
            fluid
            src='/images/uploads/b4ks-1-.png'
          )
        b-col(
          cols="12"
          md="6"
          lg="7"
        )
          h2.h3 Bikes for Kids
          p There is nothing better than a bike to help children Get Out! Bikes are an inspiring tool for positive mental, physical and emotional wellness impact. The community of Tellico Plains, TN is the gateway for scenic mountain tours, yet nearly half of the community is living below poverty with similar percentages of obesity and low education attainment.
          p Be part of the team that makes a difference in Tellico Plains to positively impact the wellness of these kids - and make an impact on the trajectory of their future!
          p A huge thank you to our partners who share our same passion for Bikes For Kids: Hincapie Sports, WEDU, The Move, Haro Bikes, Mellow Johnny's, Ski Dock &amp; Centurion Boats!
          b-btn(
            variant="primary"
            href='https://www.betterunite.com/OperationGetOut-bikesforkidstellicoplainstn'
          ) Donate

  section.who-we-are
    b-container
      b-row.mb-5(
        align-h="center"
      )
        b-col.text-center(
          cols="12"
        )
          b-img(
            src='/images/logo-short.svg'
          )
          h2.text-tertiary.mb-4 Who We Are
          div.h5.mb-4(v-html="$md.render(page.whoWeAreCopy)")

    .banner
      b-container
        b-row.bg-secondary.py-3.text-white(
          align-v="center"
        )
          b-col(
            cols="12"
            md="6"
            lg="5"
          )
            b-embed(
              type="iframe"
              aspect="16by9"
              src="https://www.youtube.com/embed/z1gD3ttcPKY"
              allowfullscreen
            )
          b-col(
            cols="12"
            md="6"
            lg="7"
          )
            h2.h3 Helping the Uvalde Kids Get Out
            p Thank you to all of the donors, volunteers, and partners that supported the Operation Get Out Bikes For Kids Uvalde by providing 800 bikes, helmets, and gear to the Robb Elementary community.

    .bg-primary
      b-container
        b-row
          b-col.text-center
            b-row.contain(
              align-h="center"
              align-v="stretch"
            )
              b-col.mb-4(
                cols="12"
                md="5"
              )
                .fill-height.bg-white
                  b-img(
                    src="/images/events.jpg"
                    fluid-grow
                  )
                  .text-center.px-4.py-5
                    h3.h5.text-primary.mb-4(
                      style='font-size: 24px'
                    ) Events
                    div(v-html="$md.render(page.eventsCopy)")
                    b-btn(
                      to="/upcoming-events"
                      variant="tertiary"
                    ) See Events

              b-col.mb-4(
                cols="12"
                md="5"
              )
                .fill-height.bg-white
                  b-img(
                    src="/images/donations.jpg"
                    fluid
                  )
                  .text-center.px-4.py-5
                    h3.h5.text-primary.mb-4(
                      style='font-size: 24px'
                    ) Donations
                    div(v-html="$md.render(page.donationsCopy)")
                    <a href="#XRDHRHMF" style="display: none"></a>

  section.about#our-story
    b-container.mb-5(
      fluid='xxl'
    )
      b-row(
        align-v="center"
      )
        b-col(
          cols="12"
          md="6"
          xl="5"
        )
          b-img-lazy(
            fluid-grow
            src="/images/book.jpg"
            max-width='599'
          )
        b-col(
          cols="12"
          md="6"
          offset-xl='1'
        )
          .eyebrow {{ page.ourStoryEyebrow }}
          h2.text-tertiary.mb-3 {{ page.ourStoryHeadline1 }}
          div(v-html="$md.render(page.ourStoryCopy1)")

    b-container.mt-5.mb-5(
      fluid='xxl'
    )
      b-row(
        align-v="center"
      )
        b-col.mb-4.mb-md-0(
          cols="12"
          md="6"
          lg="5"
        )
          h2.mb-3.text-tertiary {{ page.ourStoryHeadline2 }}
          div(v-html="$md.render(page.ourStoryCopy2)")
          //- p
          //-   strong A $30 donation includes signed copy of Blue Mind book, Operation Get Out #LetTheWaterMoveYou silicone bracelet, Blue Marble talisman, and shipping.

          //- b-btn Buy the Book

        b-col(
          cols="12"
          md="6"
          offset-lg="1"
        )
          b-embed(
            type="iframe"
            aspect="16by9"
            src="https://www.youtube.com/embed/2ANB5nDW9q8"
            allowfullscreen
          )

  section.testimonials.bg-tertiary
    b-container
      b-row
        b-col.text-center
          h2.text-white.mb-4 {{ page.testimonialsHeadline }}
          h4.text-white.mb-5(
            style="font-size: 24px; font-weight: 400"
          ) {{ page.testimonialsSubHeadline }}

      b-row
        b-col.mb-4.mb-md-0(
          cols="12"
          md="6"
          v-for="(testimonial, index) in page.testimonials"
          :key="index"
          align-v="stretch"
        )
          TestimonialCard(
            :testimonial="testimonial"
          )

  section.meet-the-team
    b-container
      b-row.mb-5
        b-col.text-center
          h2.text-tertiary Meet the team

      b-row
        b-col.mb-4(
          cols="12"
          md="4"
          lg="3"
          v-for="(member, index) in teamMembers"
          :key="index"
          align-v="strech"
        )
          TeamCard(
            :member="member"
          )

  Connect

</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('home').fetch()

    const teamMembers = await $content('team-members').sortBy('name').fetch()

    return {
      page,
      teamMembers
    }
  }
}
</script>

<style lang="scss" scoped>
.hero {
  background-image: url('/images/hero.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.hero-row {
  min-height: 600px;
}

section.banner {
  @include media-breakpoint-up(md) {
    margin-top: -80px;
  }

  .callout {
    background-image: url('/images/bike.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
}

section.who-we-are {
  padding-top: 80px;
  padding-bottom: 60px;

  .bg-primary {
    margin-top: 200px;
    padding-bottom: 60px;

    .contain {
      margin-top: -120px;
    }
  }

  .how-we-do-it {
    position: relative;
    background-color: $primary;

    @include media-breakpoint-up(lg) {
      &::after {
        content: "";
        display: block;
        width: 100px;
        height: 100%;
        background-color: $primary;
        position: absolute;
        top: 0;
        right: -100px;
      }

      &::before {
        content: "";
        display: block;
        width: 100px;
        height: 100%;
        background-color: $primary;
        position: absolute;
        top: 0;
        left: -100px;
      }
    }
  }

  .how-we-do-it-container {
    @include media-breakpoint-down(md) {
      background-color: $primary;
    }
  }
}

section.about {
  padding-top: 60px;
  padding-bottom: 60px;
}

section.testimonials {
  padding-top: 40px;
  padding-bottom: 80px;
}

section.meet-the-team {
  padding-top: 80px;
  padding-bottom: 40px;
}

</style>
