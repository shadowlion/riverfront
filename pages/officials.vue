<template lang="pug">
  section.container
    h1.text-center.pb-3 Officials
    b-card-group(columns)
      b-card(
        v-for="(official, index) in officials"
        :key="index"
        :img-src="official.imgUrl"
        img-top
      )
        b-card-text {{ official.name }}
          |
          |
          small.text-muted ({{ official.role }})
</template>

<script>
import d from "@/components/data.json";

export default {
  data() {
    return {
      officials: d.officials
    };
  }
};
</script>
