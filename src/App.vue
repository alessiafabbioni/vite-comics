<script>
import AppHeader from './components/AppHeader.vue'
import ListProducts from './components/ListProducts.vue'
import PageMenu from './components/PageMenu.vue'


export default {
  components: {
    AppHeader,
    ListProducts,
    PageMenu
  }
}
</script>

<template>
  <AppHeader/>
  <main>
    <ListProducts/>
    <PageMenu/>
  </main>
  


</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;


h1,
h2,
h3,
h4,
h5,
h6 {
  color: $primary;
}

</style>
