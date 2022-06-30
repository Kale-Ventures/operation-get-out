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
            h1.text-white Finding mental and physical wellness through nature and water.
            p.text-white OpGetOut was founded to provide the experiences and resources people need to utilize nature and water for positive mental and physical wellness.

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
            p OpGetOut is a 501c3 nonprofit with deep roots and connections in the wellness, water, military, first responder, medical and philanthropic world. What began organically — providing individuals and groups opportunities to Get Out — is now an intentional, purposeful organization.
            p.text-tertiary
              strong We plan and execute experiences, events and outings that utilize evidence-based science: nature and water can be a powerful therapeutic benefit to assist individuals and agencies dealing with loss, PTS, anxiety, grief and stress.
            p We witness the powerful unlocking and resetting that takes place when individuals are given the opportunity and tools to be empowered with the healing elements of nature and water.

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
                      fluid
                    )
                    .text-center.px-4.py-5
                      h3.h5.text-primary Events
                      p.text-gray Our events bring the community together to experience nature and discover wellness. Paddle boarding to hiking, find an event and register to join us for therapy through the great outdoors.
                      b-btn See Events
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
                      h3.h5.text-primary Donations
                      p.text-gray We function solely on donations and sponsorships which go directly to supporting outings, equipment, events and resources for individuals and agencies to learn how to benefit from nature and water as a validated wellness tool.
                      b-btn Donate

    section.about
      b-container
        b-row(
          align-v="center"
        )
          b-col(
            cols="12"
            md="6"
          )
            b-img(
              fluid-grow
              src="/images/book.jpg"
            )
          b-col(
            cols="12"
            md="6"
          )
            .eyebrow Our Story
            h2.text-tertiary.mb-3 It started out of a love of the outdoors and a need to heal.
            p We have devoted our lives to bringing individuals and groups into nature and onto the water. But when we lost two Travis County female first responders within six months of each other — StarFlight nurse Kristin McLain and Senior Deputy Jessica Hollis — we were suddenly surrounded by first responders and others dealing with loss, anxiety, depression and trauma. They turned to us for nature, water and healing —  asking us to help them heal through some of the same activities Kristin and Jessica used for their own respite.

      b-container
        b-row(
          align-v="center"
        )
          b-col.mb-4.mb-md-0(
            cols="12"
            md="6"
            lg="5"
          )
            h2.mb-3.text-tertiary Then we looked to science to validate what we were seeing.
            p A pursuit of the science and validation behind nature and water as medicine began, including guidance and partnerships with Wallace J. Nichols and the science of Blue Mind; the Global Wellness Institute; International Surf Therapy Organization; peer support advisors; and mental wellness counselors. OpGetOut is committed to helping others be intentional in using nature and water as a powerful tool for positive mental and emotional wellness impact.
            p
              strong A $30 donation includes signed copy of Blue Mind book, Operation Get Out #LetTheWaterMoveYou silicone bracelet, Blue Marble talisman, and shipping..

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

    section.testimonials.bg-tertiary
      b-container
        b-row
          b-col.text-center
            h2.text-white.mb-4 We help those in need
            h4.text-white.mb-5(
              style="font-size: 24px; font-weight: 400"
            ) We have worked with first responders, military, women, foster children, struggling youth, and individuals battling illness, grief, loss, PTS, anxiety and depression – all who continue to share amazing testimonies of how nature and water has moved, unlocked, and refreshed them.

        b-row
          b-col(
            cols="12"
            md="6"
            v-for="(testimonial, index) in testimonials"
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

    section.events(
      style="background-color: #eaf7ff"
    )
      b-container
        b-row
          b-col.text-center
            .eyebrow Events
            h2.text-tertiary.mb-5 Upcoming Events

        b-row
          b-col
            EventCard(
              v-for="(event, index) in events"
              :key="index"
              :event="event"
            )

    //- section.community
    //-   b-container
    //-     b-row
    //-       b-col.text-center
    //-         h2.text-tertiary Our Community

    section.connect
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

              b-row(
                align-h="between"
              )
                b-col(
                  cols="auto"
                )
                  h4.text-tertiary #OpGetOut

                b-col(
                  cols="auto"
                )
                  b-img.mr-3(
                    src="/images/instagram.svg"
                  )
                  b-img(
                    src="/images/facebook.svg"
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
      ],
      testimonials: [
        {
          quote: 'Operation Get Out has opened my eyes and taught me how important it is to take care of myself. It has taught me how important it is to say I’m not ok and to find help and healing through therapy and most important, to me, my blue mind!',
          attribution: 'Law Enforcement Deputy'
        },
        {
          quote: 'I cannot thank y’all enough for allowing me to join you on the water yesterday; after a year caring for COVID patients and caring for my own children during the pandemic, the water was exactly what I needed to help let it all go. This is an amazing organization!',
          attribution: 'ER Nurse'
        }
      ],
      teamMembers: [
        {
          name: 'Jen Allis'
        },
        {
          name: 'Shelby Hollis'
        },
        {
          name: 'Ricky Hollis'
        },
        {
          name: 'Martha B. Marshall, M.A., LPC'
        },
        {
          name: 'Winston Merrill'
        },
        {
          name: 'Cindy Present'
        },
        {
          name: 'Steve Present'
        }
      ],
      events: [
        {
          date: 'September 24-25, 2022',
          title: 'Get Out Girl Surf & Paddle Jam Weekend',
          location: 'Lake Austin, TX',
          body: '_An all-female weekend sharing #bluemindsisterhood! Wakesurf Saturday, Paddle Jam Sunday and weekend after party with food, DJ Coy, Boss Jaguar Surf Band, silent and live auctions with family and friends!_ \n\n Camaraderie, inspiration, and empowerment with amazing like-minded women paddling in memory and honor of Travis County first responders Kristin McLain &amp; Jessica Hollis. All proceeds provide nature and water events, experiences and equipment for front-line workers, military, nurses, surviving family and agencies through Operation Get Out, a 501c3 nonprofit.',
          image: 'surf'
        },
        {
          date: 'October 28-30, 2022',
          title: 'OpGetOut First Responder & Military Retreat',
          location: 'Canyon Lake, TX',
          body: '_An all-female weekend sharing #bluemindsisterhood! Wakesurf Saturday, Paddle Jam Sunday and weekend after party with food, DJ Coy, Boss Jaguar Surf Band, silent and live auctions with family and friends!_ \n\n Camaraderie, inspiration, and empowerment with amazing like-minded women paddling in memory and honor of Travis County first responders Kristin McLain &amp; Jessica Hollis. All proceeds provide nature and water events, experiences and equipment for front-line workers, military, nurses, surviving family and agencies through Operation Get Out, a 501c3 nonprofit.',
          image: 'military'
        }
      ]
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
  margin-top: -80px;
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
