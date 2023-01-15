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
        <input type="text">
        <button>Cerca</button>
        <!-- Nb: fare emit sul padre (App.vue), dirttamente da qui -->
        <hr>
    </div>

</template>
<style lang="scss" scoped>
.input_wrapper {
    padding: 2rem;
}
</style>