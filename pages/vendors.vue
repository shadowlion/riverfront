<template lang="pug">
  main
    b-container.py-5
      h1.text-center.pb-5 Vendors
      b-card-group(columns)
        vendor-card(
          v-for="(vendor, index) in vendors"
          :key="index"
          :vendor="vendor"
        )
</template>

<script>
import VendorCard from "@/components/VendorCard";
import d from "@/components/data.json";

export default {
  components: {
    VendorCard
  },
  data() {
    return {
      vendors: d.vendors
    };
  }
};
</script>
