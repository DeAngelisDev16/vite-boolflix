<script>
import { store } from '../store'
export default {
    name: 'AppHeader',
    //components
    data() {
        return {
            store,
        }
    }

}
</script>
<template >
    <div class="input_wrapper">
        <input type="text" v-model="store.searchedTitle">
        <button @click="$emit('searchMovie', store.searchedTitle)">Cerca</button>

        <hr>
    </div>

</template>
<style lang="scss" scoped>
.input_wrapper {
    padding: 2rem;
}
</style>