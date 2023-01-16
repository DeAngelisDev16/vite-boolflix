<script>

export default {
    name: 'movieCard',
    props: {
        movieTitle: 'string',
        originalTitle: 'string',
        movieLanguage: 'string',
        movieMark: 'number',

    },


    data() {
        return {
            imageName: 'francia.png',


        }
    },
    methods: {
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;

        }

    },




}
</script>
<template>
    <div class="movie_card">
        <!-- <ul>
            <li>{{ movieTitle }} - {{ originalTitle }} - {{ movieLanguage }} - {{ movieMark }}
            </li>
        </ul> -->
        <h2>{{ movieTitle }}</h2>
        <h4>{{ originalTitle }}</h4>
        <h6>{{ movieLanguage }}</h6>
        <img :src="getImagePath(`../assets/flags/${imageName}`)" alt="">
        <div class="movie_mark">{{ movieMark }}</div>






    </div>

</template>
<style lang="scss" scoped>
.movie_card {
    width: calc(100% / 4);
    border: 2px dashed black;
    padding: 1rem;
}
</style>