<template>
    <div class="container mt-3">
      <div class="row">
        <AlbumCard
        v-for="(elem,index) in albumData" 
        :key="index"
        :album="elem"
        />
      </div>
    </div>
</template>

<script>

import AlbumCard from './AlbumCard.vue';
import axios from 'axios'

export default {
    name: 'AlbumList',
      components: {
          AlbumCard
      },
      
      data(){
          return{
            albumData: [],
            arrayGenre: [],
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

          this.albumData.forEach((element) => {
            
            if(!this.arrayGenre.includes(element.genre))
            this.arrayGenre.push(element.genre)
          
          });

          this.$emit('emitGenre', this.arrayGenre)

        })
      }
  }
    }
</script>

<style lang="scss" scoped>

</style>