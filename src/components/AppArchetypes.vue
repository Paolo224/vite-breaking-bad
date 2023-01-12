<script>
import { store } from '../store.js'

export default {
data(){
    return{
        archetypes : null,
    }
}
}
</script>

<template>
    <div class="select">
        <select name="archetypes" id="archetypes" @change="$emit('newRequest', archetypes )" v-model="archetypes">
            <option value="Alien">Alien</option>
            <option value="Laval">Laval</option>
            <option value="Vylon">Vylon</option>
            <option value="Inzektor">Inzektor</option>
            <option value="Umi">Umi</option>
            <option value="Gusto">Gusto</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
div.select {
    padding: .4rem;

    select {
        width: 20%;
        padding: 0.3rem;
        font-size: 1.2rem;
        font-weight: 700
    }
}
</style>