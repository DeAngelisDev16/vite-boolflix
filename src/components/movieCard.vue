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


        }
    },
    methods: {
        removeLanguage() {
            const lang = document.getElementsByTagName('h6');
            lang.classlist.add('unshown');


        },
        getImagePath(imgPath) {
            if (this.store.movieList.original_language === "en") {
                this.imageName = 'uk.png';
                this.removeLanguage();

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
        <img :src="getImagePath(`../assets/flags/${imageName}`)">
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