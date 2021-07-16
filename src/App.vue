<template>
  <div id="app">

    <!-- Caricamento componente header -->
    <Header/>

    <!-- Caricamento componente main -->
    <Main/>

    <!-- Caricamento componente footer -->
    <Footer/>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
  @import './style/commons.scss';
</style>
