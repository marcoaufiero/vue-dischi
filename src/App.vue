<template>
  <div id="app">
    <nav class="col-12">
      <img src="./assets/logo.svg" alt="">
    </nav>
    <div class="container mt-5">
      <div class="row">
        <AlbumCard
        v-for="(elem,index) in albumData" 
        :key="index"
        :album="elem"
        />
      </div>
    </div>
  </div>
</template>

<script>

import AlbumCard from './components/AlbumCard';
import axios from 'axios'

export default {
  name: 'App',
  components: {
    AlbumCard
  },

  data(){
    return{
      albumData: '',
    }
    
  },

  mounted(){
    this.getApi('https://flynn.boolean.careers/exercises/api/array/music')
  },

  methods:{
    getApi(link){
      axios.get(link)
      .then((response) => {
        this.albumData = response.data.response
      })
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: sans-serif;
  background-color: #1E2D3B;
  height: 100vh;
  
  nav{
    background-color: #2E3A46;
    height: 70px;

    img{
      height: 50px;
      margin: 10px 20px;
    }

  }
}
</style>
