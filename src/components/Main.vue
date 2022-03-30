<template>
  <div>
      <div class="container-fluid">
          <div class="row" v-if="DiscsList">
              <div class="col-6 d-flex justify-content-center" v-for="(element, index) in DiscsList"
                    :key="index">
                  <DiscPage 
                    :discObject="element"/> 
              </div>
          </div> 
          <div class="row position-absolute top-50 start-50 translate-middle" v-else>
                <div class="col-12 ">
                    <div class="animate__animated animate__bounce animate__repeat-3">
                        <span class="fs-1 fw-bold text-warning" >Arrivo.....DAMMI TEMPO!</span>
                    </div>  
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
          DiscsList: null,
      }
  }, 
  created:function(){ 
      setTimeout(this.getApiDiscs, 3000)
      
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