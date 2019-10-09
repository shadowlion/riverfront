<template lang="pug">
  main
    b-container.py-5
      h1.text-center.pb-5 Officials
      b-card-group(columns)
        official-card(
          v-for="(official, index) in officials"
          :key="index"
          :official="official"
        )
</template>

<script>
import OfficialCard from "@/components/OfficialCard";
import d from "@/components/data.json";

export default {
  components: {
    OfficialCard
  },
  data() {
    return {
      officials: d.officials
    };
  }
};
</script>
