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
                Xicotencalt 523, barrio 1800
              </h3>
              <h3 class="font-weight-light mt-3">
                Telefono: 844 331 3972
              </h3>
              <h3 class="font-weight-light">
                Email: nievatecongelate@gmail.com
              </h3>
            </v-col>
            <v-col cols="12" sm="7">
              <v-form ref="form" v-model="valid" :lazy-validation="lazy" >
                <v-text-field
                    v-model="name"
                    :rules="nameRules"
                    label="Nombre"
                    required
                ></v-text-field>

                <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="E-mail"
                    required
                ></v-text-field>

                <v-textarea
                    v-model="textArea"
                    :rules="textAreaRules"
                    label="Mensaje"
                    required
                />

                <v-btn
                    :disabled="!valid"
                    color="primary"
                    :dark="valid"
                    rounded
                    block
                    class="mt-3"
                    @click="submit"
                >
                  Enviar
                </v-btn>
              </v-form>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>

    <v-snackbar
        v-model="snackbar.enabled"
        timeout="3000"
        right
        top
        :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn
            text
            v-bind="attrs"
            @click="snackbar.enabled = false"
        >
          Fecha
        </v-btn>
      </template>
    </v-snackbar>
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
  import axios from 'axios';
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
      
      let fd= new FormData();
      fd.append("key","Heintec@2021");
      fd.append("from",this.email);
      fd.append("nombre",this.name);
      fd.append("mail","nievatecongelate@gmail.com");
      fd.append("sub","He visto tu pagina web");
      fd.append("msj",this.textArea);

      console.log(fd);
      axios.post('mail/mail.php', fd).then((response) => {
         console.log(response);
         this.$refs.form.reset();
      })
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
