<template lang="pug">
  main
    section.hero.bg-tertiary
      b-container
        b-row.hero-row(
          align-v="center"
        )
          b-col(
            cols="12"
            md="6"
          )
            h1.text-white Headline about OGO’s Mission
            p.text-white Support description about mission and how you can immediately get involved with our latest endeavor and fundraiser

    section.banner
      b-container
        b-row
          b-col
            .bg-secondary.px-5.py-4
              b-row.text-white(
                align-v="center"
              )
                b-col(
                  cols="12"
                  md="8"
                  lg="9"
                )
                  h2.h4 Headline about Current Fundraiser
                  p Description of current fundraiser and summary of how to get involved and donate to specific fundraiser as well as immediate goals and effect it will have…
                b-col(
                  cols="12"
                  md="4"
                  lg="3"
                )
                  b-btn(
                    variant="primary"
                  ) Donate

    section.who-we-are
      b-container
        b-row.mb-5(
          align-h="center"
        )
          b-col.text-center(
            cols="12"
            md="10"
          )
            h2.text-tertiary Who We Are
            p.text-tertiary As a 501c3 non-profit, we have a collective passion to provide nature and Blue Mind water experiences, events and equipment to intentionally utilize the evidence-based, therapeutic benefits of being in, near, and on the water and in nature for positive mental, emotional and physical wellness impact.

      .how-we-do-it-container
        b-container
          .how-we-do-it.py-5.text-center
            h3.text-white.mb-4 How we do it
            b-row
              b-col(
                cols="12"
                md="4"
                v-for="n in 3"
              )
                .bg-white.text-center.px-4.py-5.mb-4
                  h3.h5.text-primary Events
                  p.text-gray Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor.
                  b-btn See Events

    section.about
      b-container
        b-row(
          align-v="center"
        )
          b-col(
            cols="12"
            md="6"
          )
          b-col(
            cols="12"
            md="6"
          )
            .eyebrow About Us
            h2.text-tertiary.mb-3 Our Team
            p We have spent a lifetime devoted to taking individuals and groups into nature and on the water. When we lost two of our own within six months of each other, both Travis County female first responders, StarFlight nurse Kristin McLain, to a flight rescue incident, and Senior Deputy, Jessica Hollis, to a flood incident, we were suddenly surrounded by first responders and others dealing with loss, anxiety, depression and trauma, asking us to take them to the water, just as Kristin and Jessica used the water for their own respite and release.
            p A collaborative relationship with Wallace J. Nichols and the science and understanding of Blue Mind resulted, and since then we have shared the science and unlocking power of being in, near or on the water with first responders, veterans, women, foster children, struggling youth, and individuals battling illness or grief.

    section.testimonials.bg-tertiary
      b-container
        b-row
          b-col.text-center
            h3.text-white.mb-4 Testimonials

        b-row
          b-col(
            v-for="n in 3"
            cols="12"
            md="6"
            lg="4"
          )
            TestimonialCard

    section.resources
      b-container
        b-row(
          align-v="center"
        )
          b-col.mb-4.mb-md-0(
            cols="12"
            md="6"
            lg="5"
          )
            .eyebrow Resources
            h2.mb-3.text-tertiary Our Philosophy
            p Blue Mind is at the heart of our organization. Marine biologist Dr. Wallace J. Nichols wrote a best seller about the remarkable effects of water in all of its shapes and forms on our health and well-being. Combining cutting-edge neuroscience with compelling personal stories from top athletes, leading scientists, military veterans, and gifted artists, he shows how proximity to water can improve performance, increase calm, diminish anxiety, and increase professional success. Look for our Blue Mind events coming soon.

            p
              strong A $30 donation includes signed copy of Blue Mind book, Operation Get Out #LetTheWaterMoveYou silicone bracelet, Blue Marble talisman, and shipping.

            b-btn Buy the Book
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

    section.events(
      style="background-color: #F2F5F7"
    )
      b-container
        b-row
          b-col.text-center
            .eyebrow Events
            h2.text-tertiary.mb-5 Upcoming Events

        b-row
          b-col
            EventCard

    section.community
      b-container
        b-row
          b-col.text-center
            h2.text-tertiary Our Community

    section.connect(
      style="background-color: #F2F5F7"
    )
      b-container
        b-row(
          align-h="center"
        )
          b-col.text-center(
            cols="12"
            md="6"
          )
            h2.text-tertiary.mb-5 Connect with us
            b-form(
              name="connect"
              method="POST"
              data-netlify="true"
            )
              b-row
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      type="text"
                      placeholder="First Name"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      type="text"
                      placeholder="Last Name"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      type="text"
                      placeholder="Email"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-select(
                      v-model='selected'
                      :options='options'
                      placeholder="I'm interested in..."
                    )
                b-col(
                  cols="12"
                )
                  b-form-group
                    b-form-textarea.mb-4(
                      placeholder="Write Something..."
                      no-resize
                      rows="6"
                    )

                    b-btn(
                      type="submit"
                      variant="primary"
                    ) Submit

              b-row
                b-col(
                  cols="auto"
                )
                  h4.text-tertiary #OpGetOut

                b-col(
                  cols="auto"
                )
                  b-icon(
                    icon="facebook"
                    block
                  )
</template>

<script>
export default {
  data () {
    return {
      selected: null,
      options: [
        { value: null, text: 'I\'m interested in...' },
        { value: 'Event Information', text: 'Event Information' },
        { value: 'Sponsorship opportunities', text: 'Sponsorship opportunities' },
        { value: 'Donating Equipment and Food', text: 'Donating Equipment and Food' },
        { value: 'Hosting a Get Out', text: 'Hosting a Get Out' },
        { value: 'Volunteering', text: 'Volunteering' },
        { value: 'Corporate Wellness Alignment', text: 'Corporate Wellness Alignment' },
        { value: 'All of the Above', text: 'All of the Above' },
        { value: 'Other', text: 'Other' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.hero-row {
  min-height: 600px;
}

section.banner {
  margin-top: -80px;
}

section.who-we-are {
  padding-top: 80px;
  padding-bottom: 60px;

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

section.resources {
  padding-top: 80px;
  padding-bottom: 80px;
}

section.events {
  padding-top: 40px;
  padding-bottom: 40px;
}

section.connect {
  padding-top: 60px;
  padding-bottom: 60px;
}
</style>
