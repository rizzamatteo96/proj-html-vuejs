<template>
  <div>
    <div class="container-fluid d-flex justify-content-between align-items-center px-5">
      <!-- logo + nav + btn + src -->

      <!-- importo il logo -->
      <img src="@/assets/img/logo_big.png" alt="logo" class="pointer">

      <!-- aggiungo la NavBar -->
      <nav>
        <ul class="m-0">
          <li v-for="(link,i) in navLinks" :key="i" class="d-inline-block mx-3">
            <a 
            href="#" 
            class="text-uppercase text-decoration-none"
            :class="(activePage == i)? 'fw-bold':''"> 
            {{link}} </a>
          </li>
        </ul>
      </nav>

      <!-- nella parte destra ci sono un pulsante e una lente per la ricerca -->
      <div class="right d-flex align-items-center">
        <button class="ms-btn ms-btn-light-green me-4">Purchase</button>
        <i class="fas fa-search ms-green pointer"></i>
      </div>
    </div>
  </div>  
</template>


<script>
export default {
  name : 'NavBar',
  data(){
    return{
      navLinks : ['Home','About','Services','Showcase','Blog','Contact'],
      activePage : 0
    }
  }
}
</script>

<style lang="scss">

</style>