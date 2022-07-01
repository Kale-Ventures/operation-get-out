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
          b-col.px-0.px-md-2
            .bg-secondary
              b-row.text-white(
                align-v="stretch"
                no-gutters
              )
                b-col.callout(
                  cols="12"
                  md="4"
                )
                b-col(
                  cols="12"
                  md="8"
                )
                  .p-5
                    h3.h5
                      em OpGetOut is partnering with The Move, WEDŪ, Ski Dock, Wish for Wheels &amp; Mellow Johnny’s
                    h2.h4 Bikes for Kids Uvalde supporting Robb Elementary
                    p Let’s help these kids Get Out and enjoy the wellness benefits of being on a bike! Join our mission to provide a bike and helmet for each child from Robb and Flores Elementary at the start of the school year - 750 bikes!
                    b-btn(
                      variant="light"
                      href='https://www.betterunite.com/bikesforkids-uvalde'
                    ) Donate Now

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
            p.h5.mb-4 OpGetOut is a 501c3 nonprofit with deep roots and connections in the wellness, water, military, first responder, medical and philanthropic world. What began organically — providing individuals and groups opportunities to Get Out — is now an intentional, purposeful organization.
            p.text-tertiary.h5.mb-4
              strong We plan and execute experiences, events and outings that utilize evidence-based science: nature and water can be a powerful therapeutic benefit to assist individuals and agencies dealing with loss, PTS, anxiety, grief and stress.
            p.h5.mb-4 We witness the powerful unlocking and resetting that takes place when individuals are given the opportunity and tools to be empowered with the healing elements of nature and water.

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
                      p Our events bring the community together to experience nature and discover wellness. Paddleboarding to cycling, yoga to wakesurfing, find an event and register to Get Out with us and experience wellness in the great outdoors.
                      b-btn(
                        href='#events'
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
                      p We function solely on donations and sponsorships which go directly to supporting outings, equipment, events and resources for individuals and agencies to learn how to benefit from nature and water as a validated wellness tool.
                      b-btn(
                        href='https://www.betterunite.com/bikesforkids-uvalde'
                      ) Donate

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
            .eyebrow Our Story
            h2.text-tertiary.mb-3 It started out of a love of the outdoors and a need to heal.
            p We have devoted our lives to bringing individuals and groups into nature and onto the water. But when we lost two of our own within six months of each other, StarFlight nurse Kristin McLain and Senior Deputy Jessica Hollis, both Travis County first responders, within six months of each other — StarFlight nurse Kristin McLain and Senior Deputy Jessica Hollis — we were suddenly surrounded by first responders and others dealing with loss, anxiety, depression and trauma. They turned to us for nature, water and healing —  asking us to help them heal through some of the same activities Kristin and Jessica used for their own respite.

      //- b-container.mt-5.mb-5(
      //-   fluid='xxl'
      //- )
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

    section.testimonials.bg-tertiary
      b-container
        b-row
          b-col.text-center
            h2.text-white.mb-4 We help those in need
            h4.text-white.mb-5(
              style="font-size: 24px; font-weight: 400"
            ) We have worked with first responders, military, women, foster children, struggling youth, and individuals battling illness, grief, loss, PTS, anxiety and depression – all who continue to share amazing testimonies of how nature and water has moved, unlocked, and refreshed them.

        b-row
          b-col.mb-4.mb-md-0(
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

    section.events#events(
      style="background-color: #eaf7ff"
    )
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

    //- section.community
    //-   b-container
    //-     b-row
    //-       b-col.text-center
    //-         h2.text-tertiary Our Community

    section.connect#connect
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
                  a(
                    href='https://www.instagram.com/opgetoutorg'
                  )
                    b-img.mr-3(
                      src="/images/instagram.svg"
                    )

                  a(
                    href='https://www.facebook.com/Opgetoutorg-111863733716760/'
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
          name: 'Jen Allis',
          bio: 'Instrumental in event planning and coordination, Jen has provided support for events since OGO’s inception. Jen has decades of experience in water sports activities and fully understands that water is medicine and being outdoors is critical to mental wellness. Jen is a Centurion Boats Water Warrior, mountain biker, trail runner, and wakesports coach. She also fulfills OGO operational roles including grant management and fundraising.'
        },
        {
          name: 'Ricky Hollis',
          bio: 'Ricky is an Austin Police Officer and former paramedic and Marine. He previously served as a mental health officer while on patrol for APD and now is on the Peer Support Team. He assists with running the Austin Police Honor Guard and has an active role working with the families of fallen officers. His love for the outdoors and water has not only led him to share it with others, but also spurred him to use the art of creating custom wakesurf boards, Patriot Board Co., for mental release.'
        },
        {
          name: 'Shelby Hollis',
          bio: 'Shelby began her nursing career 20 years ago in the Emergency Department and now serves as a cardiac nurse at Heart Hospital of Austin. She has worked in various areas of nursing through the years and has been privileged to help others gain needed healing. While serving as a Palliative Care Nurse Coordinator at a local trauma center during the recent pandemic, she witnessed devastating losses that only highlighted her passion to continue to getting others as well herself outdoors and on the water for both physical and mental wellness.'
        },
        {
          name: 'Martha B. Marshall, M.A., LPC',
          bio: 'Martha Marshall is a licensed counselor who utilizes nature and water as co-therapists. Her creative approach to change might include nature as a co-therapist: a walk outdoors under the oaks, a hike, or even counseling in a paddle boarding session on Austin lakes to help get in touch with the deeper, inner-knowing and strength we all forget sometimes. Her goal in work with clients is their return to balance, new perspectives, and a welcoming of their whole, wise soul. Martha presents workshops on the mind-body connection, mindful self-compassion, and family dynamics, and leads outdoor meditation experiences. She is a NADA Acudetox Specialist and NADA Registered Trainer licensed by the Texas Medical Board for acupuncture to treat addictions. Martha has NOLS Wilderness First Aid certification.'
        },
        {
          name: 'Winston Merrill',
          bio: 'As a former EMT and paramedic of 23 years, Winston has first-hand knowledge of the stresses encountered every day by first responders. After a career in EMS, Winston landed in the watersports industry. Living with the power of water, Winston has found water to be healing, whether you’re in it, around it or on it. He enjoys paddleboarding, wake surfing, and mountain biking on a regular basis and has a passion for sharing them with others for wellness impact. As an OGO founding member and a Centurion Boats Water Warrior, he is at each event assisting as driver, cyclist, coach and/or paddler while sharing his water story.'
        },
        {
          name: 'Cindy Present',
          bio: 'Cindy has spent a lifetime in the wellness, fitness and watersports industry. As a life coach, fitness trainer, watersports coach, cycling, running and Ironman athlete, motivator, and Wellness Director at Lake Austin Spa Resort, Cindy has inspired thousands to find improved mental, physical and emotional well-being. Her passion for taking individuals on the water and in nature to assist in moving them through difficult times to deeper levels of personal connection and clarity is embedded in all she does.'
        },
        {
          name: 'Steve Present',
          bio: 'Steve has over 40 years in the marine and watersports industry and was raised in Clearlake, Texas, as the son of an Air Force and NASA test pilot for the Apollo program. When Steve’s father lost his life in a test mission, Steve’s community surrounded him by water as a way for him to connect to nature, others and himself. Steve’s immersion in the watersports world began from the roots of loss, but he has spent a lifetime passing it forward, with connection and leadership in many philanthropic causes involving the use of nature and water. Steve is an avid waterskier, wakesurfer, paddleboard and mountain biker, and has received numerous awards and recognition for his role and leadership in the watersports industry, including Centurion Boats Troy Gentry Award and Water Warrior recipient.'
        }
      ],
      events: [
        {
          date: 'September 24-25, 2022',
          title: 'Get Out Girl Surf & Paddle Jam Weekend',
          location: 'Lake Austin, TX',
          body: '_An all-female weekend sharing #bluemindsisterhood! Wakesurf Saturday, Paddle Jam Sunday and weekend after party with food, DJ Coy, Boss Jaguar Surf Band, silent and live auctions with family and friends!_ \n\n Camaraderie, inspiration, and empowerment with amazing like-minded women paddling in memory and honor of Travis County first responders Kristin McLain &amp; Jessica Hollis. All proceeds provide nature and water events, experiences and equipment for front-line workers, military, nurses, surviving family and agencies through Operation Get Out, a 501c3 nonprofit.',
          image: 'surf',
          buttonText: 'Register',
          url: 'https://www.betterunite.com/OperationGetOut-9thannualgetoutgirlsurfpaddlejamweekend'
        },
        {
          date: 'October 28-30, 2022',
          title: 'OpGetOut First Responder & Military Retreat',
          location: 'Canyon Lake, TX',
          body: 'A weekend retreat providing nature and water experiences with boating, wake surfing, lakeside yoga, and paddleboarding, good food and good music for front line responders and military at the beautiful Canyon Lakeview Resort, Canyon Lake, Texas.',
          image: 'military',
          buttonText: 'More Info',
          url: 'mailto:cindy@getoutgirl.com'
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
