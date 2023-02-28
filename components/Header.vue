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
  b-navbar-toggle.mr-3.mr-md-0(
      target="nav-collapse"
    )
  b-collapse#nav-collapse.ml-auto.px-3.px-lg-0(
    is-nav
  )
    b-navbar-nav.ml-auto.d-flex.align-items-end
      b-nav-item(
        to="#our-story"
      ) Our Story
      b-nav-item(
        to="/upcoming-events"
      ) Upcoming Events
      b-nav-item(
        to="/past-events"
      ) Past Events
      b-nav-item(
        to="#connect"
      ) Connect
      b-nav-item(
        to="#XRDHRHMF"
      ) Donate

</template>

<style lang="scss" scoped>
.navbar {
  background-color: rgba(255, 255, 255, 0.85);

  li a {
    font-size: 18px;
    color: white;
  }
}

::v-deep .nav-item {
  @include media-breakpoint-down(md) {
    width: 50%;
    text-align: flex-start;
    background-color: #004883;
    padding-left: 3em;
  }
}

::v-deep .nav-link {
  text-transform: none;
  font-size: 20px;
  color: white;
  margin-right: 25px;
}

::v-deep .navbar-toggler {
  border: none;
}
</style>
