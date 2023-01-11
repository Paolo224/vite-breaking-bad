<script>
export default {
    name : 'AppHeader',
    data(){
        return{

        }
    },
    methods : {

    }
}
</script>

<template>
    <div class="logo">
        <img src="http://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="">
    </div>
    <h1>
        Yu-Gi-Oh Api
    </h1>
</template>

<style lang="scss" scoped>
    div.logo{
        width: 10%;
        display: flex;
        align-items: center;

        img{
            width: 100%;
        }
    }

    h1{
        padding-left: 1rem;
    }
</style>