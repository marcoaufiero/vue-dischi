<template>
  <div id="app">
    <HeaderComp/>
    <MainComp/>
  </div>
</template>

<script>

import MainComp from './components/MainComp.vue';
import HeaderComp from './components/HeaderComp.vue'


export default {
  name: 'App',
  components: {
    MainComp,
    HeaderComp
  },

  
}
</script>

<style lang="scss">
#app {
  font-family: sans-serif;
  background-color: #1E2D3B;
  height: 100vh;
  
  
}
</style>
