<template>
  <div>
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

    </div>
    <!-- fine header bottom -->
  </div>
</template>


<script>
export default {
  name : 'Header'
}
</script>


<style lang="scss">
  .header-top{
    background-color: #3d3d3d;

    .container{
      height: 50px;

      .left > *,
      .right > *{
        margin: 0 10px;
      }
    }
  }
</style>