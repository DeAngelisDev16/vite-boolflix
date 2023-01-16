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
        <ul>
            <li>{{ movieTitle }} - {{ originalTitle }} - {{ movieLanguage }} - {{ movieMark }}
            </li>





        </ul>
    </div>

</template>
<style lang="scss" scoped>

</style>