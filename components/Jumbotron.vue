<template lang="pug">
  .jumbotron.jumbotron-fluid.bg-pic.text-center.mb-0.text-light.bg-variant-transparent
    b-container
      h1.display-3.d-none.d-md-block Riverfront Dancesport Festival
      h1.display-4.d-block.d-md-none Riverfront Dancesport Festival
      p.lead Come celebrate our 10th year along the Riverfront!
      hr.my-4.border-light
      p.pb-5.text-left Riverfront Dancesport Festival is the best run and most friendly Dancesport competition in Greater Cincinnati. Regardless of your dancing level, we offer competition for all levels in all styles. Our 10th anniversary will be held on January 11, 2020, so don’t miss out!
      b-button(variant="info" to="/forms" size="lg") Register!
</template>

<style scoped>
.bg-pic {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 1)),
    url("~assets/hero.webp");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
