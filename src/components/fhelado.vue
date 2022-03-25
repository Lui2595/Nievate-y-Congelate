<template>
<div class=" row">
  <div>
    <br>
    <flipper
      width="270px"
      height="300px"
      :flipped="flipped"
      @click="onClick"
    >
      <div slot="front">
        <v-card
          :loading="loading"
          class="mx-auto my-12"
          max-width="374"
        >
          <v-card-title>Paletas de agua</v-card-title>

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
                •Fresa
                •Pica fresa rellena chamoy
                •Naranja con chile
                •Mango
                •Mango relleno de chamoy
                •Coco
                •Tamarindo
                •Tamarindo rellenda de chamoy
                •Limon
                •Limon rellena de chamoy
                •Piña
                •Piña rellena de chamoy
                •Michelada
                •Paleta de diablito
                •Pepino con Chile
                •Sandia
                •Sandia con chile
            </div>
            
          </v-card-text>
          
        </v-card>
      </div>
    </flipper>
    <br>
  </div>
  
</div>
</template>

<script>
import Flipper from 'vue-flipper';

export default {
  components: { Flipper },
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
