<template lang="pug">
  main
    b-container.py-5
      b-row
        b-col
          h1.pb-5.text-center Forms
      b-row
        b-col
          b-table-lite(striped hover :fields="fields" :items="items" caption-top)
            template(#table-caption) Look below to view or download the forms you need to register:
            template(#cell(download_link)="data")
              a(:href="data.item.download" _target="blank" download)
                download-cloud-icon
</template>

<script>
import { DownloadCloudIcon } from "vue-feather-icons";

export default {
  components: {
    DownloadCloudIcon
  },
  data() {
    return {
      fields: [
        "file_name",
        "notes",
        { key: "download_link", class: "text-center" }
      ],
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
