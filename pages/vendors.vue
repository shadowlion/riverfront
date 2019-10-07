<template lang="pug">
  .container.py-3
    h1.text-center.pb-3 Vendors
    b-card-group(columns)
      b-card(
        v-for="(vendor, index) in vendors"
        :key="index"
        :img-src="vendor.imgSrc"
        img-top
        :title="vendor.name"
      )
        b-card-text
          b-link(
            v-if="vendor.phone"
            :href="`tel:${vendor.phone}`"
          ) {{ vendor.phone }}
        b-card-text
          b-link(
            v-if="vendor.email"
            :href="`mailto:${vendor.email}`"
          ) {{ vendor.email }}
        b-card-text
          b-link(
            v-if="vendor.site"
            :href="vendor.site"
          ) Website
        b-card-text.small.text-muted {{ vendor.role }}
</template>

<script>
import d from "@/components/data.json";

export default {
  data() {
    return {
      vendors: d.vendors
    };
  }
};
</script>
