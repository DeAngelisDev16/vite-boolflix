<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import { store } from '../src/store'

export default {
    name: 'App',
    components: {
        AppHeader,
        AppMain

    },
    data() {
        return {
            store,
            apiUrl: 'https://api.themoviedb.org/3/movie/550?api_key=f38ef18ffb95138a318e7a1901a728d7',
        }
    },
    methods: {
        getMovies() {
            axios.get(this.apiUrl, {
                params: {
                    //ID: 12345
                }
            })
                .then(function (response) {
                    console.log(response.data);
                    store.movieList = response.data;
                    console.log(store.movieList)
                })
                .catch(function (error) {
                    console.log(error);
                })
                .then(function () {
                    // always executed
                });
        }

    },
    created() {
        this.getMovies()


    }

}

</script>

<template>
    <AppHeader />
    <AppMain />


</template>

<style lang="scss">
@use './styles/general.scss' as *;
</style>
