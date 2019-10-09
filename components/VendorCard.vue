<template lang="pug">
  b-card(:img-src="require(`@/assets/vendors/${vendor.imgSrc}`)" img-top)
    b-card-title {{ vendor.name }}
    b-card-text.my-0
      b-link(
        v-if="vendor.phone"
        :href="`tel:${vendor.phone}`"
      ) {{ vendor.phone }}
    b-card-text.my-0
      b-link(
        v-if="vendor.email"
        :href="`mailto:${vendor.email}`"
      ) {{ vendor.email }}
    b-card-text.mb-4
      b-link(
        v-if="vendor.site"
        :href="vendor.site"
      ) Website
    b-card-text.small.text-muted {{ vendor.role }}
</template>

<script>
export default {
  props: {
    vendor: {
      type: Object,
      default() {},
      imgSrc: {
        type: String,
        required: true
      },
      name: {
        type: String,
        required: true
      },
      email: {
        type: String,
        required: false
      },
      phone: {
        type: String,
        required: false
      },
      site: {
        type: String,
        required: false
      },
      role: {
        type: String,
        required: true
      }
    }
  }
};
</script>
