<template>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://static.comunicae.com/photos/notas/1213578/1585920783_heladoshop.jpg',
          },
          {
            src: 'https://www.infobae.com/new-resizer/JuaBk6KaLFmzsnErCQbLgG-vgt4=/1200x900/filters:format(jpg):quality(85)//arc-anglerfish-arc2-prod-infobae.s3.amazonaws.com/public/NR5TRNFLTZHEJOZVGSRV6FJ4RQ.jpg',
          },
          {
            src: 'https://sevilla.abc.es/gurme/wp-content/uploads/sites/24/2016/07/recetasconhelado.jpg',
          },
          {
            src: 'https://i.ytimg.com/vi/6Zi9TMTgCbk/maxresdefault.jpg',
          },
          
        ],
      }
    },
  }
</script>
