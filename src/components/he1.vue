<template>
<div class=" row">
  <div>
    <br>
    <flipper1
      width="370px"
      height="400px"
      :flipped="flipped"
      @click="onClick"
    >
      <div slot="front">
        <v-card
          :loading="loading"
          class="mx-auto my-12"
          max-width="374"
        >
          <v-card-title>Helado</v-card-title>

          <v-img
            height="250"
            src="../assets/img/h1.jpg"
            
          ></v-img>
        </v-card>
      </div>

      <div slot="back">
        <v-card
          :loading="loading"
          class="mx-auto my-12"
          max-width="auto"
        >
          <template slot="progress">
            <v-progress-linear
              color="deep-purple"
              height="10"
              indeterminate
            ></v-progress-linear>
          </template>

          <v-card-text>
            <v-row
              align="center"
              class="mx-0"
            >

              <div class="grey--text ml-15">
                Sabores
              </div>
            </v-row>

            <div class="my-4 subtitle-1">
                <div class="row">
                <div class="col-6">
                  •Fresa
•Mango
•Coco
•Nuez
•Melón 
•Chocolate
•Galleta oreo
•Queso zarzamora
•Fresas con crema
•Gansito
                  
                </div>
                <div class="col-6">
                •Chocoroles
•Pinguino 
•Napolitano
•Piña colada 
•Vainilla
•Almendra
•Queso
                </div>
              </div>
            </div>


          </v-card-text>
          
        </v-card>
      </div>
    </flipper1>
    <br>
  </div>
  
</div>
</template>

<script>
import Flipper1 from 'vue-flipper';

export default {
  components: { Flipper1 },
  data () {
    return {
      flipped: false
    };
  },
  methods: {
    onClick () {
      this.flipped = !this.flipped;
    }
  }
};
</script>

<style src="vue-flipper/dist/vue-flipper.css" />
