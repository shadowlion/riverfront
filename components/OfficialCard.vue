<template lang="pug">
  b-card
    //- b-card-img(:src="require(`@/assets/officials/${official.imgSrc}`)" top)
    b-card-text {{ official.name }}
      |
      |
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
  }
};
</script>
