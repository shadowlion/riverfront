<template lang="pug">
  main
    jumbotron
    section-goal
    showcase-content
</template>

<script>
import Jumbotron from "@/components/Jumbotron";
import SectionGoal from "@/components/SectionGoal";
import ShowcaseContent from "@/components/ShowcaseContent";

export default {
  components: {
    Jumbotron,
    SectionGoal,
    ShowcaseContent
  }
};
</script>
