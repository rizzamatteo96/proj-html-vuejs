<template>
  <div class="section2">
    <div class="container-fluid my-5 py-5">
      <div class="row g-0 align-items-center">
        <!-- img + text -->
        <!-- inizio parte sinistra -->
        <div class="cont-imgs col-7 left pe-5 position-relative">
          <div class="position-relative">
            <img src="@/assets/img/business-man.jpg" alt="business man">
            <div class="overlay"></div>
          </div>
          <img class="img-first" src="@/assets/img/business-woman.jpg" alt="business woman">
        </div>
        <!-- fine parte sinistra -->

        <!-- inizio parte destra -->
        <div class="col-5 right p-5">
          <div class="title fw-bold">
            learn more about our <span class="ms-green">missions</span>
          </div>

          <div class="divider my-5"></div>

          <div class="text-secondary mb-3">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.</div>

          <button class="ms-btn ms-btn-light-green mt-5">
            <span class="btn-overlay"></span>
            <span class="btn-text">Read more</span>
          </button>
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

    img{
      border-radius: 20px;
      box-shadow: 0 0 30px lightgray;
      width: 70%;
    }

    .title{
      font-size: 3rem;
      font-family: "Quicksand";
    }
  }

  .cont-imgs{
    left: -30px;
    margin-bottom: 120px;

    .overlay{
      position: absolute;
      top: 0;
      left: 0;
      width: 70%;
      height: 100%;
      border-radius: 20px;
      background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
    }

    .img-first{
      position: absolute;
      top: 100px;
      left: 30%;
    }
  }
</style>