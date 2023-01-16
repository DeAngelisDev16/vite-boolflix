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


        getImagePath(imgPath) {
            if (this.languages.includes(this.store.movieList.original_language)) {
                this.imageName = this.store.movieList.original_language;


            } else;
            return new URL(imgPath, import.meta.url).href;


        }

    },




}
</script>
<template>
    <div class="movie_card">

        <h2>{{ movieTitle }}</h2>
        <h4>{{ originalTitle }}</h4>
        <h6>{{ movieLanguage }}</h6>
        <img :src="getImagePath(`../public/flags/${imageName}.png`)">
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