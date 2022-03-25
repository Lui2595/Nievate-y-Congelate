<template>
  <div class="home">
    
     <carousel />
      <home />
      <about />
      <download />
     
  </div>
</template>

<style scoped>


</style>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
// import navigation from "@/components/Navigation";
// import foote from "@/components/Footer";
import home from "@/components/HomeSection";
import about from "@/components/AboutSection";
import download from "@/components/DownloadSection";
//import contact from "@/components/ContactSection";
import carousel from "@/components/Carousel"

export default {
  name: 'Home',
  components: {
    
    home,
    about,
    download,
   // contact,
    carousel,
  }, created(){
        document.title = "Nievate y Congelate"    }
}
</script>
