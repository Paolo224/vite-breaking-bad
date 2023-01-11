<script>
import { store } from '../store.js'
import axios from 'axios'

export default {
    name: 'AppMain',
    data() {
        return {
            store,
            yuGiHoList : [],
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
                    this.yuGiHoList = response.data.data;
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
    <div v-for="element in yuGiHoList">
        {{ element.name }}
    </div>
</template>

<style lang="scss" scoped>

</style>