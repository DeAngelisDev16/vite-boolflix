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


        }
    }




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
        <div class="movie_mark">{{ movieMark }}</div>
        <img src="https://flagcdn.com/40x30/za.png" srcset="https://flagcdn.com/80x60/za.png 2x,
    https://flagcdn.com/120x90/usa.png 3x" width="40" height="30" alt="Usa">





    </div>

</template>
<style lang="scss" scoped>
.movie_card {
    width: calc(100% / 4);
    border: 2px dashed black;
    padding: 1rem;
}
</style>