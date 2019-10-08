<template lang="pug">
  main
    b-container.py-5
      b-row
        b-col
          h1.pb-5.text-center Need to Contact Us?
      b-row
        b-col.d-none.d-md-block
        b-col
          ul.list-unstyled
            b-media.py-3(
              tag="li"
              v-for="(contact, index) in contacts"
              :key="index"
            )
              template(#aside)
                b-img(
                  thumbnail
                  width="100"
                  v-if="contact.img && contact.img.length > 0"
                  :src="require(`@/assets/contact/${contact.img}`)"
                )
                b-img(
                  thumbnail
                  blank
                  blank-color="#abc"
                  width="100"
                  v-else
                )
              h4.mt-0.mb-1 {{ contact.name }}
              p.text-muted ({{ contact.role }})
              address
                | Phone:
                |
                |
                a(:href="`tel:${contact.phone}`") {{ contact.phone }}
                br
                | Email:
                |
                |
                a(:href="`mailto:${contact.email}`") {{ contact.email }}
                div(v-if="contact.fax")
                  | Fax:
                  |
                  |
                  a(:href="`tel:${contact.fax}`") {{ contact.fax }}
        b-col.d-none.d-md-block
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        {
          img: "gert.jpg",
          name: "Gert Roslender",
          role: "Organizer",
          phone: "317-566-0028",
          email: "gertro@sbcglobal.net"
        },
        {
          img: "bill.jpg",
          name: "Bill Sparks",
          role: "Organizer",
          phone: "614-204-0196",
          email: "DanceSparks@aol.com"
        },
        {
          img: "",
          name: "Brenda Burger",
          role: "Registrar",
          phone: "740-969-2431",
          email: "CompBrenda@aol.com",
          fax: "740-969-4457"
        }
      ]
    };
  }
};
</script>
