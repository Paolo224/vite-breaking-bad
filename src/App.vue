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
@use 'bootstrap/scss/bootstrap.scss' as *;

main{
  max-width: 1000px;
  border: 2px solid red;
  margin: 0 auto;
}
</style>
