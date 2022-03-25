<template>
  <section>
    <br>
    <br>
    <br>
    
<v-card>
    <v-toolbar
      color= '#5b3910'
      dark
      flat
    >
     
        <v-tabs
          v-model="tabs"
          centered
        >
          <v-tab
            v-for="n in titulo"
            :key="n"
          >
             {{ n }}
          </v-tab>
        </v-tabs>
      
    </v-toolbar>

    <v-tabs-items v-model="tabs">
      <v-tab-item>
        <v-card >
          <v-card-text>
            <div class="ml-8 row">
             <fp1 />
             <fp2 />
             <fp3 />
            </div>
            <div class="ml-8 row">
              <fp4 />
            </div>
            <br>
            <br>
            <br>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-title class="headline">
            
          </v-card-title>
          <v-card-text>
            <div class="ml-15 row">
             <he1 />
             <he2 />
             <n1 />
            </div>
            <br>
            <br>
            <br>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-title class="headline">
         
          </v-card-title>
          <v-card-text>
            <div class="ml-15 row">
             <o1 />
             <o2 />
             <o3 />
            </div>
            <br>
            <br>
            <br>
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
  </section>
</template>


  <script>
  
  import fp1 from "./fp1";
  import fp2 from "./fp2";
  import fp3 from "./fp3";
  import fp4 from "./fp4";
  import he1 from "./he1";
  import he2 from "./he2";
  import n1 from "./n1";
  import o1 from "./o1";
  import o2 from "./o2";
  import o3 from "./o3";


  
  export default {
    components: {
    fp1,
    fp2,
    fp3,
    fp4,
    he1,
    he2,
    n1,
    o1,
    o2,
    o3
    
  },
    data () {
      return {
        tabs: null,
        text: 'texto.',
        titulo:['Paletas','Helado / Nieve','Otros',

      ]
      }
    },
  }
</script>


<style>

</style>
