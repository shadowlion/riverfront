<template lang="pug" functional>
  main
    b-container.py-5
      h1.pb-5.text-center Venue Information
      b-row
        b-col.pb-3(md="6" sm="12")
          b-img(
            thumbnail
            fluid
            src="~assets/venues/hotel1.jpg"
          )
        b-col(md="6" sm="12")
          p The dance venue and hotel for the 2020 Riverfront Dancesport Festival is at the beautiful
            |
            |
            a(href="https://www.hyatt.com/en-US/hotel/ohio/hyatt-regency-cincinnati/cinci") Hyatt Regency Cincinnati
            |
            |
            | in downtown Cincinnati. Please book your room as soon as possible. When booking, please mention that you are with the Riverfront Dancesport Festival to take advantage of available room discounts. Be sure to use the group code
            |
            |
            strong G-ARDS
            |
            |
            | and enter the dates appropriate for the 2020 Riverfront Dancesport Festival (e.g. Jan. 10-11).
          p
            address
              strong Hotel Location:
              br
              | Hyatt Regency Cincinnati
              br
              | 151 West Fifth Street
              br
              | Cincinnati, Ohio, USA  45202
              br
              | Phone:
              |
              |
              b-link(href="tel:5135791234") (513)-579-1234
              br
              b-link(href="https://www.hyatt.com/en-US/hotel/ohio/hyatt-regency-cincinnati/cinci") Website
              |
              |
              | (Map info and directions available)
      b-row
        b-col.py-2(md="4" sm="12")
          b-img(
            thumbnail
            fluid
            src="~assets/venues/hotel2.jpg"
          )
        b-col.py-2(md="4" sm="12")
          b-img(
            thumbnail
            fluid
            src="~assets/venues/hotel3.jpg"
          )
        b-col.py-2(md="4" sm="12")
          b-img(
            thumbnail
            fluid
            src="~assets/venues/hotel4.jpg"
          )
</template>

<script>
export default {
  functional: true
};
</script>
