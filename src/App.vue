<template>
  <div id="app">

    <!-- Caricamento componente header -->
    <Header/>

    <!-- Caricamento componente main -->
    <Main/>

    <!-- Caricamento componente footer -->
    <Footer/>

    <!-- Caricamento componente chat -->
    <Chat/>

    <!-- Caricamento componente scroll top -->
    <ScrollTop :enable="enableScrollTop"/>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Chat from './components/Chat.vue'
import ScrollTop from './components/ScrollTop.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Chat,
    ScrollTop
  },
  data(){
    return{
      enableScrollTop : false
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll(){
      (window.scrollY > 500) ? this.enableScrollTop = true : this.enableScrollTop = false;
    }
  }
}
</script>

<style lang="scss">
  @import './style/commons.scss';
</style>
