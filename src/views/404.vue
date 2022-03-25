<template>
    <div class="404">
        <tab />
    </div>
</template>

<script>
import tab from "@/components/404";

export default {
   name: '404',
  components: {
    
   tab,
    
  }, created(){
        document.title = "Not Found"    }
}
</script>
}