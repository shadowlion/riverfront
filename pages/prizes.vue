<template lang="pug">
  main
    b-container.py-5
      h1.text-center.pb-5 Prizes
      b-row
        b-col.d-none.d-md-block
        b-col(cols="12" md="5")
          prize-card.my-4(
            v-for="(prize, index) in prizes"
            :key="index"
            :prize="prize"
          )
        b-col.d-none.d-md-block
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
