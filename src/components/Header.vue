<template>
  <header>
    <!-- inizio header top -->
    <div class="header-top text-white">
      <!-- inizio contenitore -->
      <div class="container d-flex justify-content-between align-items-center">

        <!-- inizio parte sx -->
        <div class="left">
          <i class="fas fa-phone-alt"></i>
          <span>(001) 88451234</span>
        </div>
        <!-- fine parte sx -->

        <!-- inizio parte dx -->
        <div class="right">
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-pinterest-p"></i>
        </div>
        <!-- fine parte dx -->

      </div>
      <!-- fine contenitore -->
    </div>
    <!-- fine header top -->

    <!-- inizio header bottom -->
    <div class="header-bottom">
      <!-- Caricamento NavBar -->
      <NavBar/>
    </div>
    <!-- fine header bottom -->
  </header>
</template>


<script>
import NavBar from './NavBar.vue'
export default {
  name : 'Header',
  components : {
    NavBar
  }
}
</script>


<style lang="scss">
  @import '@/style/header.scss';
</style>