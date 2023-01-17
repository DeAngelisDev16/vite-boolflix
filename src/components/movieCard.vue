<script>
import { store } from '../store';

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
            store,
            imageName: '',
            languages: ['it', 'en', 'es', 'fr'],


        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(`../assets/flags/${imgPath}.png`, import.meta.url).href;
        }



    },




}
</script>
<template>
    <div class="movie_card">

        <h2>{{ movieTitle }}</h2>
        <h4>{{ originalTitle }}</h4>
        <!-- <h6>{{ movieLanguage }}</h6> -->
        <img v-if="languages.includes(movieLanguage)" :src="getImagePath(movieLanguage)">
        <span v-else>{{ movieLanguage }}</span>
        <div class="movie_mark">{{ movieMark }}</div>






    </div>

</template>
<style lang="scss" scoped>
.movie_card {
    width: calc(100% / 4);
    border: 2px dashed black;
    padding: 1rem;

    img {
        width: 15%;
    }
}
</style>