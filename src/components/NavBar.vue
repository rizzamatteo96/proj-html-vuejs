<template>
  <div>
    <div class="container d-flex justify-content-between align-items-center">
      <!-- logo + nav + btn + src -->

      <!-- importo il logo -->
      <img src="@/assets/img/logo_big.png" alt="logo">

      <!-- aggiungo la NavBar -->
      <nav>
        <ul class="m-0">
          <li v-for="(link,i) in navLinks" :key="i" class="d-inline-block mx-3">
            <a href="#" class="text-uppercase text-decoration-none text-dark"> {{link}} </a>
          </li>
        </ul>
      </nav>

      <!-- nella parte destra ci sono un pulsante e una lente per la ricerca -->
      <div class="right d-flex align-items-center">
        <button class="ms-btn-light-green">Purchase</button>
        <i class="fas fa-search ms-green"></i>
      </div>
    </div>
  </div>  
</template>


<script>
export default {
  name : 'NavBar',
  data(){
    return{
      navLinks : ['Home','About','Services','Showcase','Blog','Contact']
    }
  }
}
</script>

<style lang="scss">

</style>