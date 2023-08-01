<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <page-index msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import pageIndex from './view/pageIndex'

export default {
  name: 'App',
  components: {
    pageIndex
  }
}
</script>

<style>
body{
  padding: 0;
  margin: 0;
}
#app {
  font-family: PuHuiTi,Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
  /* margin-top: 60px; */
}

@font-face {  

font-family: 'PuHuiTi';

src: url('./assets/font/AlibabaPuHuiTi-3-55-Regular.ttf');
font-weight: normal;  
font-style: normal;  
}
</style>
