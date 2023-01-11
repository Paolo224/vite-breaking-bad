<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'
import AppCards from './components/AppCards.vue'

export default{
  components : {
    AppHeader,
    AppMain,
    AppCards,
  }
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
    <AppCards />
  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;

header{
  background-color: white;
  margin-bottom: 1rem;
}

main{
    max-width: 1000px;
    margin: 0 auto;
}
</style>
