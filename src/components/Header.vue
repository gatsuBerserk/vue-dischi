<template>
  <div> 
    <nav class="navbar navbar-light my-bg">
      <div class="container-fluid">
        <img src="../assets/img/logo.svg" alt="">
        <select v-model="selectGenre" class="form-select my-select" aria-label="Default select example"  @change="$emit('selezione',selectGenre)">
          <option disable value="">Select for...</option>
          <option   :value="genre[index]" v-for="(element, index) in genre" :key="index">{{genre[index]}} </option>
        </select>
      </div>  
  </nav> 
      <h1 class="text-white">hai selezionato: {{selectGenre}}</h1>
  </div>
</template>

<script>
export default { 
  name : "HeaderPage", 
  props: ["genre"],
  data : function(){
    return{
      selectGenre:"",
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/my-style.scss"; 
  .my-bg{
    background-color:rgb(46, 58, 70) ;
  } 
  img{
    height: 50px;
  } 

  .my-select{
    width: 20%;
  }
</style>