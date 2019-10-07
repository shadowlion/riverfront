<template lang="pug">
  main
    b-container.py-5
      b-row
        .col-3.d-none.d-sm-block
        b-col
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
