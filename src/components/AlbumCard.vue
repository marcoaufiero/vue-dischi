<template>
    <div class="ms-card text-white">
        <div class="ms-img-box row">
            <img :src="album.poster" alt="">
        </div>
        <div class="ms-info-box text-center">
            <div class="ms-card-title">
                <h6>{{album.title.toUpperCase()}}</h6>
            </div>
            <div>
                <span>{{album.author}}</span>
            </div>
            <div>
                <span>{{album.year}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AlbumCard',
        props: {
            album: Object,
        }
    }
</script>

<style lang="scss" scoped>

    .ms-card{
        background-color: #2E3A46;
        margin: 20px 20px;
        width: calc(100% / 5 - 40px);

        .ms-img-box{

            padding: 10px 5px;
            margin-bottom: 20px;

            img{
                width: 100%;
                aspect-ratio: 1/1;
            }
        }

        span{
            color: grey;
        }
        
    }

</style>
