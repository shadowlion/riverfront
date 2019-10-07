<template lang="pug">
  b-jumbotron.bg-pic.text-center.mb-5(
    text-variant="light"
    bg-variant="transparent"
    fluid
  )
    template(slot="header") Riverfront Dancesport Festival
    template(slot="lead") Come celebrate our 10th year along the Riverfront!
    hr.my-4.border-light
    p.pb-5.text-left Riverfront Dancesport Festival is the best run and most friendly Dancesport competition in Greater Cincinnati. Regardless of your dancing level, we offer competition for all levels in all styles. Our 10th anniversary will be held on January 11, 2020, so don’t miss out!
    b-button(variant="info" to="/forms" size="lg") Register!
</template>

<style scoped>
.bg-pic {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.9)),
    url("~assets/hero.webp");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
