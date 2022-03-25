<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      dark
      src="@/assets/img/bgDrawer.jpg"
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="@/assets/img/logo.png"  alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Menu</v-list-item-title>
            <v-list-item-subtitle>Movil</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="isCatalogo();$vuetify.goTo(link)"
        >
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
              text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <router-link :to="'catalogo'">
        <v-list-item>
          <v-list-item-icon class="justify-center">
            <v-icon></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">
              Catalogo
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        </router-link>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      :flat="flat"
      dark
      class="px-15"
      :class="{ expand: flat }"
    >
      <v-toolbar-title>
        <v-img src="@/assets/img/logoletras.png" max-width="300px" />
      </v-toolbar-title>
      <v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-4"
        v-if="isXs"
      />
      <div v-else>
        
          <v-btn text @click="isCatalogo();$vuetify.goTo('#carousel');">
            <span class="mr-2">inicio</span>
          </v-btn>
        <v-btn text @click="isCatalogo();$vuetify.goTo('#hero');">
          <span class="mr-2">Promo</span>
        </v-btn>
        <v-btn text @click="isCatalogo();$vuetify.goTo('#features');">
          <span class="mr-2">Productos</span>
        </v-btn>
        <v-btn text @click="isCatalogo();$vuetify.goTo('#about');">
          <span class="mr-2">Sobre Nosotros</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">Contactanos</span>
        </v-btn>
        <router-link :to="'catalogo'">
          <v-btn rounded outlined text >
            <span class="mr-2">Catalogo</span>
          </v-btn>
        </router-link> 
      </div>
    </v-app-bar>
  </div>
</template>

<style scoped>
.v-toolbar {
  transition: 0.6s;
}

.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>

<script>
export default {
  data: () => ({
    drawer: null,
    isXs: false,
    items: [
      ["", "Inicio", "#carousel"],
      ["", "Promo", "#hero"],
      ["", "Productos", "#features"],
      ["", "Catergoria", "#download"],
      ["", "Contactanos", "#contact"],
     
    ],
    

  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
      isCatalogo(){
      if( this.$route.name === "Catalogo"){
       // alert("hola");
        this.$router.push('/');
      }
      
    }
  },
  computed:{
  
  },
  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
};
</script>
