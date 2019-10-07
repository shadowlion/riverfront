<template lang="pug">
  #app
    #nav
      nav-bar
    #main-content
      nuxt
    #footer
      base-footer
</template>

<script>
import NavBar from "@/components/NavBar";
import BaseFooter from "@/components/BaseFooter";

export default {
  components: {
    NavBar,
    BaseFooter
  }
};
</script>
