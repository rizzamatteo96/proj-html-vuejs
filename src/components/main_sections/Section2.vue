<template>
  <div class="section2">
    <div class="container-fluid my-5">
      <div class="row row-cols-2 g-0 align-items-center">
        <!-- img + text -->
        <!-- inizio parte sinistra -->
        <div class="left pe-5">
          <img class="w-100 p-3" src="@/assets/img/business-woman.jpg" alt="business woman">
        </div>
        <!-- fine parte sinistra -->

        <!-- inizio parte destra -->
        <div class="right p-5">
          <div class="title fw-bold fs-1">
            learn more about our <span class="ms-green">missions</span>
          </div>

          <div class="divider my-5"></div>

          <div class="text-secondary mb-3">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptatem sit asperiores praesentium fugiat molestias inventore quibusdam laboriosam deleniti maiores quod ad explicabo magnam cumque, id tempore laudantium, similique exercitationem odit!</div>

          <button class="ms-btn ms-btn-light-green">Read more</button>
        </div>
        <!-- fine parte destra -->
      </div>


    </div>
  </div>
</template>


<script>
export default {
  name : 'Section2'
}
</script>


<style lang="scss">
  .section2{
    background-color: #f9f9f9;
  }
</style>