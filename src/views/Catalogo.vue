<template>
  <div class="catalogo">
   <tab />
  </div>
</template>

<style scoped>

</style>
<script>
import tab from "@/components/Tab";

export default {
   name: 'Catalogo',
  components: {
    
    tab,
    
  }, created(){
        document.title = "Catalogo"    }
}
</script>
