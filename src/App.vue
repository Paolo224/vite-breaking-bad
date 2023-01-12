<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'

export default{
  components : {
    AppHeader,
    AppMain,
  }
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;

header{
  background-color: white;
  margin-bottom: 1rem;
  display: flex;
  height: 70px;
  align-items: center;
}

main{
    max-width: 1000px;
    margin: 0 auto;
}
</style>
