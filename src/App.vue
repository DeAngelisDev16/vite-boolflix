<script>
//import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import { store } from '../src/store'

export default {
    name: 'App.vue',
    components: {
        AppHeader,
        AppMain

    },
    data() {
        return {
            store,
        }
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
