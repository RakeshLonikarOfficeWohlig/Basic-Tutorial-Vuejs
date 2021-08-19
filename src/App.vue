<template>
  <div id="app">
    <!-- <Home /> -->
    <!-- <Eventhandling /> -->
    <Democom />
   

    
  </div>
</template>

<script>
// import Home from './components/Home'
// import Eventhandling from './components/Eventhandling'
import Democom from './components/Democom.vue'


export default {
  name: 'App',
  components: {
    // Home,
    // Eventhandling,
    Democom,
   
   
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
  margin-top: 60px;
}
</style>
