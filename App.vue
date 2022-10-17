<template>
  <div id="app">
    <router-view></router-view>
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="vue2"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import "@/assets/js/rem.js"
import "@/utils/rem.js"
export default {
  name: 'App',
  components: {},
    // HelloWorld
  
  created(){
    // console.log(window.innerWidth,document.documentElement.clientWidth,'---------') 
    // let  dWidth = window.innerWidth || document.documentElement.clientWidth 
    //                     || document.body.clientWidth
    // let dHeight = window.innerHeight || document.documentElement.clientHeight 
    //                     || document.body.clientHeight

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 5px;
}


</style>
