<script>
import { store } from '../store.js'
import axios from 'axios'
import AppCards from './AppCards.vue'
import AppArchetypes from './AppArchetypes.vue'

export default {
    name: "AppMain",
    data() {
        return {
            store,
        };
    },
    methods: {
        getElementYuGiHo(archetypes) {
            axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0 ", {
                params: {
                    archetype : archetypes 
                }
            })
                .then((response) => {
                console.log(response.data.data);
                this.store.yuGiHoList = response.data.data;
            })
                .catch(function (error) {
                console.log(error);
            });
        },
    },
    created() {
        this.getElementYuGiHo();
    },
    components: { 
        AppArchetypes,
        AppCards,
    }
}
</script>

<template>
    <AppArchetypes @newRequest="getElementYuGiHo" />
    <div class="counter-cards">
        Found {{ store.yuGiHoList.length }} cards
    </div>
    <AppCards />
</template>

<style lang="scss" scoped>
    div.counter-cards{
        background-color: black;
        color: white;
        width: 100%;
        text-align: center;
        padding: .5rem;
    }
</style>