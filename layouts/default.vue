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

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
