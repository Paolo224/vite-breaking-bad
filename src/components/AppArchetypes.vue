<script>
export default {

}
</script>

<template>
    <div>
        <select name="archetypes" id="archetypes" @keyup.enter="$emit('newRequest')">
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

</style>