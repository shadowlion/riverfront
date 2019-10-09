<template lang="pug">
  b-card(:img-src="imgFile" img-top)
    b-card-text {{ official.name }}
      br
      small.text-muted ({{ official.role }})
</template>

<script>
export default {
  props: {
    official: {
      type: Object,
      default() {},
      imgSrc: {
        type: String,
        required: false
      },
      name: {
        type: String,
        required: true
      },
      role: {
        type: String,
        required: true
      }
    }
  },
  computed: {
    imgFile() {
      return this.official.imgSrc ? `/officials/${this.official.imgSrc}` : "";
    }
  }
};
</script>
