<template lang="pug">
  main
    b-container.py-5
      h1.pb-5.text-center Forms
      b-alert(show)
        p.pt-3 Registration and entry forms should be completed and sent in as soon as possible. Please make checks payable to the "Riverfront Dancesport Festival" and mail all completed forms and payment to:
          address
            strong Riverfront Dancesport Festival
            br
            | 7227 Edenborough Court
            br
            | Lancaster, OH 43130
          | If there are any questions on registration, contact
          |
          |
          nuxt-link(to="/contact") Brenda.
          |
          |
          | You can also fax her all the completed registration and entry forms, but payment will need to be sent to above mail address, along with a copy of the same completed registration and entry forms.
        p If there’s a problem contacting the Registrar, you may call
          |
          |
          nuxt-link(to="/contact") Bill Sparks
          |
          |
          | instead (8am-8pm EST).
      b-alert(show variant="info")
        p To qualify and earn additional points for Early Rewards, entries and payments must be received by December 15, 2019.
        p.mb-0 Normal entry deadline is December 31, 2019.
      b-alert(show variant="warning") Competitor Entry Fee and Package Pricing forms are password-protected. Contact
        |
        |
        nuxt-link(to="/contact") Brenda
        |
        |
        | for the password.
      b-table-lite(striped hover :fields="fields" :items="items" caption-top)
        template(#table-caption) Look below to view or download the forms you need to register:
        template(#cell(download)="data")
          a(
            :href="`/docs/2020/2020RF${data.item.download}.pdf`"
            _target="blank"
          )
            download-cloud-icon
</template>

<script>
import { DownloadCloudIcon } from "vue-feather-icons";
import d from "@/components/data.json";

export default {
  components: {
    DownloadCloudIcon
  },
  data() {
    return {
      fields: ["file_name", "notes", { key: "download", class: "text-center" }],
      items: d.docs
    };
  }
};
</script>
