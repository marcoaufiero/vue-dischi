<template>
    <main>
        <div class="container mt-5">
            <select name="" id="">
                <option value="">genre</option>
            </select>
        </div>
        
        <AlbumList/>
    </main>
</template>

<script>
    
import AlbumList from './AlbumList.vue'
    
    export default {
        name: 'MainComp',
        components: {
            AlbumList
        },

        mounted(){
            
        }
        
    }
</script>

<style lang="scss" scoped>
    
    main{
        height: 100vh -70px;
    }

</style>