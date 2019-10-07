<template lang="pug">
  .container.py-5
    .row
      .col
        h1 Forms
    .row
      .col
        b-table-lite(striped hover :fields="fields" :items="items" caption-top)
          template(slot="table-caption") Look below to view or download the forms you need to register:
          template(slot="[download]" slot-scope="data")
            a(:href="data.item.download" _target="blank" download) Download
</template>

<script>
export default {
  data() {
    return {
      fields: ["file_name", "notes", "download"],
      items: [
        {
          file_name: "Waiver/Release Form",
          notes: "Early Bird deadline 12/31/2019",
          download:
            "http://riverfrontdancesportfestival.com/downloads/2019RFWaiverReleaseForm.pdf"
        },
        {
          file_name: "General Admission Form",
          download:
            "http://riverfrontdancesportfestival.com/downloads/2019RFWaiverReleaseForm.pdf"
        },
        {
          file_name: "Spectator/Admission Form",
          download:
            "http://riverfrontdancesportfestival.com/downloads/2019RFWaiverReleaseForm.pdf"
        },
        {
          file_name: "Summary Form",
          download:
            "http://riverfrontdancesportfestival.com/downloads/2019RFWaiverReleaseForm.pdf"
        }
      ]
    };
  }
};
</script>
