<template>
<div class=" row">
  <div>
    <br>
    <flipper2
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
          <v-card-title>Paletas de crema</v-card-title>

          <v-img
            height="250"
            src="../assets/img/p2.jpg"
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
                  •Fresa rellena de lechera
                  •Fresas con crema
                  •Mango
                  •Mango rellena de lechera
                  •Coco
                  •Coco rellena de lechera
                  •Nuez 
                  •Nuez rellena de lechera
                  •Nuez rellena de cajeta
                  •Kiwi
                  •Kiwi rellena de lechera
                  •Chocolate
                  
                </div>
                <div class="col-6">
                  •Galleta oreo
                •Queso zarzamora
                •Queso zarzamora rellena de  lechera
                •Queso rellena de cajeta
                •Melón
                •Vainilla
                •Vainilla rellena de lechera
                •Vainilla rellena de cajeta 
                •Frutos secos
                •Gansito
                •Chocoroles
                •Pinguino
                •Duvalin
                </div>
              </div>
            </div>
            Fresa


          </v-card-text>
          
        </v-card>
      </div>
    </flipper2>
    <br>
  </div>
  
</div>
</template>

<script>
import Flipper2 from 'vue-flipper';

export default {
  components: { Flipper2 },
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
