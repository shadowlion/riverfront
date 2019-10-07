<template lang="pug">
  b-navbar.py-3(toggleable="sm" type="dark" variant="dark")
    b-container
      b-navbar-brand(href="/") RDF
      b-navbar-toggle(target="nav-collapse")
      b-collapse#nav-collapse(is-nav)
        b-navbar-nav.ml-auto
          b-nav-item(
            v-for="(link, index) in sidebarLinks"
            :key="index"
            :to="link.url"
          ) {{ link.title }}
</template>

<script>
export default {
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
