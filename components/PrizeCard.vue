<template lang="pug">
  b-card(no-body)
    template(#header) {{ prize.title }}
    b-list-group(flush)
      b-list-group-item(
        v-for="(item, index) in prize.list"
        :key="index"
      ) {{ index + 1 }}: {{ item }}
    b-card-body(v-if="prize.text")
      b-card-text {{ prize.text }}
</template>

<script>
export default {
  props: {
    prize: {
      type: Object,
      default() {},
      title: {
        type: String,
        required: true
      },
      list: {
        type: Array,
        default() {},
        required: false
      },
      text: {
        type: String,
        required: false
      }
    }
  }
};
</script>
