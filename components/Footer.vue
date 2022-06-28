<template lang="pug">
  footer.text-white
    b-container
      b-row
        b-col.mb-4.mb-md-0.text-center.text-lg-left(
          cols="12"
          md="6"
          lg="3"
        )
          nuxt-link(
            to="/"
          )
            b-img-lazy(
              height="44"
              width="196"
              src="/svgs/logo-white.svg"
            )

        b-col.mb-4.mb-md-0.text-center.text-lg-left(
          cols="6"
          lg="3"
        )
          .section-title Locations
          nuxt-link(
            to="/locations/abilene"
          ) Abilene
          nuxt-link(
            to="/locations/san-angelo"
          ) San Angelo

        b-col.text-center.text-lg-left(
          cols="6"
          lg="3"
        )
          nuxt-link(
            to="/faq"
          ) FAQs
          nuxt-link(
            to="/contact"
          ) Contact
          a(
            href="https://laundryluv.careerplug.com/jobs/1569194/apps/new"
            target="_blank"
          ) Careers

        b-col.text-center.text-lg-left(
          cols="12"
          md="6"
          lg="3"
        )
          .section-title Follow Us
          a.d-inline-block.mr-3(
            href="https://www.facebook.com/laundryluv/"
            target="_blank"
          )
            b-img-lazy(
              height="25"
              width="25"
              src="/svgs/facebook.svg"
            )
          a.d-inline-block(
            href="https://www.instagram.com/laundryluv"
            target="_blank"
          )
            b-img-lazy(
              height="25"
              width="25"
              src="/svgs/instagram.svg"
            )

      b-row
        b-col
          p.copyright.text-center.text-lg-left &copy;{{new Date().getFullYear()}} LaundryLuv. All Rights Reserved.
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss">
footer {
  padding-top: 55px;
  padding-bottom: 55px;
  background-color: $tertiary;

  .text-h6 {
    font-size: 16px;
    text-transform: uppercase;
    font-weight: 500;
  }

  a {
    display: block;
    text-transform: uppercase;
    font-weight: $font-weight-bold;
    text-decoration: none;
    color: inherit;

    &:hover {
      color: $secondary;
    }
  }

  .section-title {
    font-family: $bitter;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.13em;
  }

  .copyright {
    margin-top: 40px;
    font-size: 16px;
    font-weight: 400;

    @include media-breakpoint-up(md) {
      margin-top: 80px;
    }
  }
}
</style>
