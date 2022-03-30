<template>
  <div> 
    <nav class="navbar navbar-light my-bg">
      <div class="container-fluid">
        <img src="../assets/img/logo.svg" alt="">
      </div>
  </nav>
  </div>
</template>

<script>
export default { 
  name : "HeaderPage",

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
</style>