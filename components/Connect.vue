<template lang="pug">
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
              input(type="hidden" name="form-name" value="connect")
              b-row
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      name="first_name"
                      type="text"
                      placeholder="First Name"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      name="last_name"
                      type="text"
                      placeholder="Last Name"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-input(
                      name="email"
                      type="text"
                      placeholder="Email"
                    )
                b-col(
                  cols="12"
                  md="6"
                )
                  b-form-group
                    b-form-select(
                      name="interest"
                      v-model='selected'
                      :options='options'
                      placeholder="I'm interested in..."
                    )
                b-col(
                  cols="12"
                )
                  b-form-group
                    b-form-textarea.mb-4(
                      name="text"
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

</script>

<style lang="scss" scoped>

section.connect {
  padding-top: 60px;
  padding-bottom: 60px;
}

</style>
