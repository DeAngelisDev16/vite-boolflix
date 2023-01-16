<script>
import { store } from '../store';
import movieCard from './movieCard.vue';
export default {
    name: 'AppMain',
    components: {
        movieCard

    },
    data() {
        return {
            store,
        }
    }

}
</script>
<template >
    <div class="movie_preview_wrapper">
        <movieCard v-for="movie in store.movieList" :movieTitle="movie.title" :originalTitle="movie.original_title"
            :movieLanguage="movie.original_language" :movieMark="movie.vote_average" />


    </div>


</template>
<style lang="scss" scoped>
.movie_preview_wrapper {
    padding: 2rem;
    display: flex;
    flex-wrap: wrap;



}
</style>