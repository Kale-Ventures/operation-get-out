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
            h3.text-white Testimonials

        b-row
          b-col(
            cols="12"
            md="6"
            lg="4"
          )
            .bg-white

    section.resources
      b-container
        b-row
          b-col(
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

    section.events(
      style="background-color: #F2F5F7"
    )
      b-container
        b-row
          b-col.text-center
            .eyebrow Events
            h2.text-tertiary Upcoming Events

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
            h2.text-tertiary Connect with us
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
                  b-form-input(
                    type="text"
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
</template>

<style lang="scss" scoped>
.hero-row {
  min-height: 600px;
}

section.about {
  padding-top: 60px;
  padding-bottom: 60px;
}

section.testimonials {
  padding-top: 40px;
  padding-bottom: 40px;
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
