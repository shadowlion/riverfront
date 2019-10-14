<template lang="pug">
  div
    h1.text-center Schedule
      br
    h6.text-center.text-muted (Subject to change)
    hr.my-5
    h2.pb-4 January 10, 2020
      |
      |
      small.text-muted (Friday)
    schedule-table(:items="fridayEvening")
    hr.my-5
    h2.pb-3 January 11, 2020
      |
      |
      small.text-muted (Saturday)
    schedule-table(:items="saturdayMorning")
      template(#sessionTitle)
        h3.py-3 Morning Session
    b-alert(variant="info" show) Lunch will be served 12:00pm - 2:00pm
    schedule-table(:items="saturdayAfternoon")
      template(#sessionTitle)
        h3.py-3 Afternoon Session
    b-alert(variant="info" show) Dinner will be served 5:30pm - 7:30pm
    schedule-table.pb-4(:items="saturdayEvening")
      template(#sessionTitle)
        h3.py-3 Evening Session
    .text-muted
      small
        | *After Party tickets + Pre-Competition Seminar are included with Packages A & B.
        br
        | *A-La-Carte After Party tickets are available for purchase at the Registration desk.
        br
        | *If performing a Solo or Formation, music can only be accepted via Flash Drive.
</template>

<script>
import d from "./data.json";
import ScheduleTable from "./ScheduleTable";

export default {
  components: {
    ScheduleTable
  },
  data() {
    return {
      fridayEvening: d.schedule.friday,
      saturdayMorning: d.schedule.saturday.morning,
      saturdayAfternoon: d.schedule.saturday.afternoon,
      saturdayEvening: d.schedule.saturday.evening
    };
  }
};
</script>
