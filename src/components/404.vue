<template>
  <section class="pb-8" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="12" sm="5">
              <h1 class="font-weight-light display-1">Contactanos</h1>
              <h3 class="font-weight-light mt-3">
                Para informacion y cotizaciones favor de contactarnos.
              </h3>
              <h3 class="font-weight-light mt-3">
                xicotencalt 523, barrioo 1800
              </h3>
              <h3 class="font-weight-light mt-3">
                Telefono: xxx xxx-xx-xx
              </h3>
              <h3 class="font-weight-light">
                Email: nievateycongelate@gmail.com
              </h3>
            </v-col>
            <v-col cols="12" sm="7">
             
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>


  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

</style>

<script>
// import {db} from '@/main'

export default {
  data: () => ({
    icons: ["fa-facebook", "fa-twitter", "fa-linkedin", "fa-instagram"],
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "Este campo es obligatorio",
      (v) => (v && v.length >= 6) || "El nombre debe tener 6 caracteres minimo",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail es obligatorio",
      (v) => /.+@.+\..+/.test(v) || "E-mail no valido",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "Este campo es obligatorio",
      (v) => (v && v.length >= 10) || "Minimo 10 caracteres",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  methods: {
    submit() {
      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensage enviado con exito"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Error al enviar mensaje"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    }
  }
};
</script>
