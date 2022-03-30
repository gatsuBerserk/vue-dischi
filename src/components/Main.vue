<template>
  <div>
      
      <DiscPage/> 
      
      
  </div>
</template>

<script> 
import DiscPage from "./DiscPage.vue"

export default {
    name: "MainPage", 
    components: { 
        DiscPage,
        
  }
}
</script>

<style lang="scss" scoped>
 @import "@/style/my-style.scss";
</style>