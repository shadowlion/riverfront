<template lang="pug">
  main
    b-container.py-5
      h1.text-center.pb-5 Prizes
      b-card-group(columns)
        prize-card(
          v-for="(prize, index) in prizes"
          :key="index"
          :prize="prize"
        )
</template>

<script>
import d from "@/components/data.json";
import PrizeCard from "@/components/PrizeCard";

export default {
  components: {
    PrizeCard
  },
  data() {
    return {
      prizes: d.prizes
    };
  }
};
</script>
