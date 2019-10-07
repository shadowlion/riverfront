<template lang="pug">
  .container.py-5
    .row
      .col-3.d-none.d-sm-block
      .col
        schedule-content
      .col-3.d-none.d-sm-block
</template>

<script>
import ScheduleContent from "../components/ScheduleContent";

export default {
  components: {
    ScheduleContent
  }
};
</script>
