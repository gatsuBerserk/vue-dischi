<template>
  <div>
      <div class="container-fluid">
          <div class="row">
              <div class="col-12">
                  <h1>Prova</h1>
                  <DiscPage/> 
              </div>
          </div>
      </div>
      
      
      
  </div>
</template>

<script> 
// import axios from "axios";
import DiscPage from "./DiscPage.vue"

export default {
    name: "MainPage", 
    components: { 
        DiscPage,   
  },
}
</script>

<style lang="scss" scoped>
 @import "../assets/style/my-style.scss";  

 h1{
     color: white;
 }

</style>