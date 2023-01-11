<script>
import { store } from '../store.js'

export default {
    name: 'AppCards',

    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <section class="cards">
        <div class="card" v-for="element in store.yuGiHoList">
            <img :src="element.card_images[0].image_url" alt="">
            <div class="card-text">
                {{ element.name }}
                <p v-if="element.archetype">
                    {{ element.archetype }}
                </p>
                <p v-else>
                    Archetipo non definito
                </p>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
section.cards {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    background-color: white;
    padding: 1rem;
}

div.card {
    width: calc((100% / 5) - 1rem);
    margin: 1rem .5rem;
    text-align: center;

    img {
        width: 100%;
    }

    div.card-text {
        background-color: #d48f38;
        padding: .4rem;
        height: 75px;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        p {
            color: black;
            font-weight: 700;
        }
    }
}
</style>