<script>
import { store } from '../store';
export default {
    name: 'AppMain',
    //components
    data() {
        return {
            store,
        }
    }

}
</script>
<template >
    <div class="movie_preview_wrapper">
        <ul>
            <li v-for="movie in store.movieList">{{ movie.title }}</li>
        </ul>

    </div>


</template>
<style lang="scss" scoped>
.movie_preview_wrapper {
    padding: 2rem;
}
</style>