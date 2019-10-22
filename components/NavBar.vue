<template lang="pug">
  b-navbar.py-3(toggleable="sm" type="dark" variant="dark")
    b-container
      b-navbar-brand(href="/")
        b-img(:src="require(`@/assets/logo.png`)" height="50" alt="RDF")
      b-navbar-toggle(target="nav-collapse")
      b-collapse#nav-collapse(is-nav)
        b-navbar-nav.ml-auto
          b-nav-item(
            v-for="(link, index) in sidebarLinks"
            :key="index"
            :to="link.url"
          ) {{ link.title }}
          b-nav-item(
            href="https://facebook.com/riverfrontdancesportfestival"
          )
            facebook-icon
</template>

<script>
import { FacebookIcon } from "vue-feather-icons";

export default {
  components: {
    FacebookIcon
  },
  data() {
    return {
      sidebarLinks: [
        {
          title: "Home",
          url: "/"
        },
        {
          title: "Forms",
          url: "/forms"
        },
        {
          title: "Schedule",
          url: "/schedule"
        },
        {
          title: "Prizes",
          url: "/prizes"
        },
        {
          title: "Officials",
          url: "/officials"
        },
        {
          title: "Vendors",
          url: "/vendors"
        },
        {
          title: "Venue",
          url: "/venue"
        },
        {
          title: "Contact",
          url: "/contact"
        }
      ]
    };
  }
};
</script>
