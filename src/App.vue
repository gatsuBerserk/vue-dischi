<template>
  <div id="app">
    <Header/> 
    <Main/>
  </div>
</template>

<script>
import Header from "./components/Header.vue" 
import Main from "./components/Main.vue"

export default {
  name: 'App',
  components: {
    Header, 
    Main,
  }
}
</script>

<style lang="scss">
  @import "@/assets/style/my-style.scss";  
  #app{
    background-color: rgb(30, 45, 59); 
    height: 100vh;
  }

</style>
