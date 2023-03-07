<template lang="pug">
b-navbar.p-0(
  sticky
  toggleable="lg"
)
  b-navbar-brand.ml-4.my-2(
    to="/"
  )
    b-img(
      src="/images/logo.png"
      height="30"
    )
  b-navbar-toggle.mr-3.mr-md-0.my-2(
    target="nav-collapse"
  )
  b-collapse#nav-collapse.ml-auto.px-3.px-lg-0(
    is-nav
  )
    b-navbar-nav.ml-auto.d-flex.align-items-center
      b-nav-item(
        href='/#our-story'
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
.navbar-collapse {
  @include media-breakpoint-down(md) {
    background-color: $tertiary;
    padding: 20px 0;
  }
}

.navbar {
  background-color: rgba(255, 255, 255, 0.85);

  @include media-breakpoint-down(md) {
    padding-bottom: 0;
  }

  li a {
    font-size: 18px;
    color: white;
  }
}

::v-deep .nav-link {
  font-size: 20px;
  margin-right: 25px;

  @include media-breakpoint-down(md) {
    color: white !important;
  }
}

::v-deep .navbar-toggler {
  border: none;
}

::v-deep .nuxt-link-active {
  font-weight: 600;

  @include media-breakpoint-up(lg) {
    color: $tertiary !important;
  }
}
</style>
