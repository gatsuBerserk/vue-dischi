<template>
  <div> 
    <nav class="navbar navbar-light my-bg">
      <div class="container-fluid">
        <img src="../assets/img/logo.svg" alt="">
        <select class="form-select my-select" aria-label="Default select example">
          <option selected>Select for...</option>
          <option value="element" v-for="(element, index) in genre" :key="index">{{genre[index]}}</option>
        </select>
      </div>  
  </nav> 
  
  </div>
</template>

<script>
export default { 
  name : "HeaderPage", 
  props: ["genre"],
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