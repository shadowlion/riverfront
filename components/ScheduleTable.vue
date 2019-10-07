<template lang="pug">
  div
    slot(name="sessionTitle")
    b-table-lite(striped hover :items="items" thead-class="d-none")
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true
    }
  }
};
</script>
