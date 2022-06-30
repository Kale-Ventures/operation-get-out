<template lang="pug">
b-navbar.px-0(
  sticky
  toggleable="lg"
)
  //- b-navbar-toggle(
  //-   target="nav-collapse"
  //- )
  //-   b-img(
  //-     src="/svgs/hamburger.svg"
  //-     width="40"
  //-     height="24"
  //-   )
  b-navbar-brand.ml-4(
    to="/"
  )
    b-img(
      src="/images/logo.png"
      height="30"
    )
  b-collapse#nav-collapse.ml-auto.px-3.px-lg-0(
    is-nav
  )
    b-navbar-nav.ml-auto.d-flex.align-items-center
      b-nav-item.text-primary(
        to="/contact"
      ) About
      b-nav-item(
        to="/contact"
      ) Resources
      b-nav-item(
        to="/contact"
      ) Events
      b-nav-item(
        to="/contact"
      ) Community
      b-nav-item(
        to="/contact"
      ) Connect
  b-btn.mr-1.mr-md-4 Donate

</template>

<style lang="scss" scoped>
.navbar {
  background-color: rgba(255, 255, 255, 0.85);
}

::v-deep .nav-link {
  text-transform: uppercase;
  font-size: 16px;
  color: $primary !important;
  margin-right: 25px;
}

::v-deep .navbar-toggler {
  border: none;
}
</style>
