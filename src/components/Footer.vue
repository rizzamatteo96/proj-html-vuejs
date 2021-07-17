<template>
  <div class="footer">

    <!-- inizio footer top -->
    <div class="container-fluid">
      <div class="top">

      </div>
    </div>
    <!-- fine footer top -->

    <!-- inizio footer bottom -->
    <div class="bottom d-flex justify-content-between align-items-center text-white px-5">
      <div class="left text-uppercase">
        &copy; 2020 Phlox business theme.
      </div>
      <div class="right">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-pinterest-p"></i>
      </div>
    </div>
    <!-- fine footer bottom -->

  </div>
</template>


<script>
export default {
  name : 'Footer'
}
</script>


<style lang="scss">
  .footer{

    .bottom{
      height: 100px;
      background-image: linear-gradient(to right, rgb(54, 54, 54) , black);

      .right > *{
        margin: 0 10px;
      }
    }
  }
</style>