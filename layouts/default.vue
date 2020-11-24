<style lang="scss">
  #app {
    font-family: 'Roboto', sans-serif;
    color: $tertiary;
    background-color: $primary;
    min-height: 100vh;
    z-index: -10;
  }
</style>
<template>
  <div id="app">
      <navbar/>
      <nuxt />
      <page-footer/>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar'
import PageFooter from '~/components/Footer'

export default {
  components: {
    Navbar,
    PageFooter
  }
}
</script>
