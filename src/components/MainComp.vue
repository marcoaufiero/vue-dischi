<template>
    <main>
        <div class="container mt-5">
            <select name="" id="" v-model="selectedGenre">
                <option v-for="(elem,index) in arrayGenre" :key="index" :value="elem">{{elem}}</option>
            </select>
        </div>
        
        <AlbumList @emitGenre="methodsGenre"/>
    </main>
</template>

<script>
    
import AlbumList from './AlbumList.vue'
    
    export default {
        name: 'MainComp',
        components: {
            AlbumList
        },

        data(){
            return{
                arrayGenre: [],
                selectedGenre: ''
            }
        },

        mounted(){
            
        },

        methods: {
            
            methodsGenre(arrayGenre){
                this.arrayGenre = arrayGenre
            }
        }
        
    }
</script>

<style lang="scss" scoped>
    
    main{
        height: 100vh -70px;
    }

</style>