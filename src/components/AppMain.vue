<script>
import { store } from '../store.js'
import axios from 'axios'

export default {
    name: 'AppMain',
    data() {
        return {
            store,
        }
    },
    methods: {
        getElementYuGiHo() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0 ', {
                params: {
                }
            })
                .then((response) => {
                    console.log(response.data.data);
                    this.store.yuGiHoList = response.data.data;
                })
                .catch(function (error) {
                    console.log(error);
                })
        }
    },
    created() {
        this.getElementYuGiHo();
    },
}
</script>

<template>
    <div class="counter-cards">
        Found {{ store.yuGiHoList.length }} cards
    </div>
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