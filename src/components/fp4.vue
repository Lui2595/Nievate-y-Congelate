<template>
<div class=" row">
  <div>
    <br>
    <flipper3
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
          <v-card-title>Maxi paletas</v-card-title>

          <v-img
            height="250"
            src="../assets/img/p4.jpeg"
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
              •Mango
              •Limon
              •Pepino
              •Tamarindo
              •Grosella 
              •Chicle
              •Uva 
              •Coco
            </div>
            
          </v-card-text>
          
        </v-card>
      </div>
    </flipper3>
    <br>
  </div>
  
</div>
</template>

<script>
import Flipper3 from 'vue-flipper';

export default {
  components: { Flipper3 },
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
