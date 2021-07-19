<template>
  <div class="h-100">

    <div class="row h-100 ps-5 pe-3">
      <!-- lato sinistro - testo -->
      <div class="col-6 d-flex flex-column justify-content-center">
        <!-- anni di esperienza -->
        <div class="experience text-uppercase ms-green fw-bold fs-5">17 years of experience</div>

        <!-- titolo diviso in due sezioni -->
        <div class="title fw-bold fs-1">
          <div>{{cardInfomations.mainTitleTop}}</div>
          <div>
            {{cardInfomations.mainTitleBot}} 
            <span class="ms-green">{{cardInfomations.mainTitleGreen}}</span>
          </div> 
          
        </div>

        <!-- divisore tratteggiato -->
        <div class="divider my-5"></div>

        <!-- paragrafo di spiegazione -->
        <p>{{cardInfomations.paragraf}}</p>

        <!-- pulsante read more -->
        <div class="read-more my-5">
          <button class="ms-btn ms-btn-black">Read more</button>
        </div>

        <!-- link ai social -->
        <div class="social text-uppercase fs-6 fw-bold mt-5">
          <a href="#">Facebook</a>
           - 
          <a href="#">Instagram</a>
           - 
          <a href="#">Youtube</a>
           - 
          <a href="#">Twitter</a>
        </div>
      </div>

      <!-- lato destro - immagine -->
      <div class="col-6 altezza"  v-bind:style="{ backgroundImage: 'url(' + cardInfomations.img + ')' }"> </div>
    </div>

  </div>
</template>


<script>
export default {
  name : 'Card',
  props : {
    'cardInfomations' : Object
  }
}
</script>


<style lang="scss">
  .altezza{
    height: 1000px;
    background-position: left center;
  }
</style>