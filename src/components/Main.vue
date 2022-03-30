<template>
  <div>
      <div class="container-fluid">
          <div class="row">
              <div class="col-6 d-flex justify-content-center" v-for="(element, index) in DiscsList"
                    :key="index">
                  <DiscPage 
                    :discObject="element"/> 
              </div>
          </div>
      </div>
      
      
      
  </div>
</template>

<script> 
import axios from "axios";
import DiscPage from "./DiscPage.vue"

export default {
    name: "MainPage", 
    components: { 
        DiscPage,   
  },
  data: function(){
      return{
          DiscsList: "",
      }
  }, 
  created:function(){
      this.getApiDiscs()
  },
  methods: {
      getApiDiscs(){
          axios.get("https://flynn.boolean.careers/exercises/api/array/music") 
            .then((response) => { 
                this.DiscsList = response.data.response; 
                console.table(this.DiscsList);
            }) 
            // in caso qualcosa non funzionasse 
            .catch((error) =>{
                console.log(error);
            })
        }
    }
}
</script>

<style lang="scss" scoped>
 @import "../assets/style/my-style.scss";  

 h1{
     color: white;
 }

</style>