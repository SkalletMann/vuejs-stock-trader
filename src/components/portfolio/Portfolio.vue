<template>
    <div>
        <app-stock v-for="stock in stocks" :stock="stock" :key="stock.id"></app-stock>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';
    import AppStock from './Stock.vue';

    export default {
        components: {
            AppStock
        },
        computed: {
            ...mapGetters({
                stocks: 'stockPortfolio'
            })
        }    
    }
</script>

<style scoped>

</style>
