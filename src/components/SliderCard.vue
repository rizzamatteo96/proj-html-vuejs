<template>
  <div class="h-100 slider-card">

    <div class="row h-100 ps-5 w-100 position-relative overflow-hidden"
    :class="activeClass">
      <!-- lato sinistro - testo -->
      <div class="col-6 altezza d-flex flex-column justify-content-center">
        <!-- anni di esperienza -->
        <div class="experience text-uppercase position-relative ms-green fw-bold fs-5">17 years of experience</div>

        <!-- titolo diviso in due sezioni -->
        <div class="title fw-bold">
          <div>{{cardInfomations.mainTitleTop}}</div>
          <div>
            {{cardInfomations.mainTitleBot}} 
            <span class="ms-green">{{cardInfomations.mainTitleGreen}}</span>
          </div> 
        </div>

        <!-- divisore tratteggiato -->
        <div class="divider my-5"></div>

        <!-- paragrafo di spiegazione -->
        <p class="card-infos">{{cardInfomations.paragraf}}</p>

        <!-- pulsante read more -->
        <div class="read-more my-5">
          <button class="ms-btn ms-btn-black">
            <span class="btn-overlay"></span>
            <span class="btn-text">Read more</span>
          </button>
        </div>

        <!-- link ai social -->
        <div class="social text-uppercase fs-6 fw-bold mt-5">
          <a href="#">Facebook</a>
          <span class="mx-3">-</span>
          <a href="#">Instagram</a>
          <span class="mx-3">-</span>
          <a href="#">Youtube</a>
          <span class="mx-3">-</span>
          <a href="#">Twitter</a>
        </div>
      </div>

      <!-- lato destro - immagine -->
      <!-- <div class="col-6 altezza"  v-bind:style="{ backgroundImage: 'url(' + cardInfomations.img + ')' }"> -->
      <img :src="cardInfomations.img" alt="img slider" class="slider-img">
    </div>

  </div>
</template>


<script>
export default {
  name : 'Card',
  props : {
    'cardInfomations' : Object,
    'activeClass' : String
  }
}
</script>


<style lang="scss">
  .slider-card{
    .title{
      font-size: 5rem;
      position: relative;
      z-index: 99;
      opacity: 0;
    }
  
    .card-infos{
      position: relative;
      z-index: 99;
      opacity: 0;
    }

    .read-more button{
      position: relative;
      z-index: 99;
      transform: scale(0);
    }
  
    .slider-img{
      position: absolute;
      top: 50%;
      left: 80%;
      transform: translate(-50%, -50%) scale(0);
      width: 75% !important;
      z-index: 9;
    }
  
    .active{
      .title{
        animation-name: loadTitle;
        animation-delay: 0s;
        animation-duration: 1s;
        animation-fill-mode: forwards;
      }
  
      .card-infos{
        animation-name: loadInfos;
        animation-delay: 0.25s;
        animation-duration: 0.75s;
        animation-fill-mode: forwards;
      }

      .read-more button{
        animation-name: loadButton;
        animation-delay: 0.7s;
        animation-duration: 1s;
        animation-fill-mode: forwards;
        transform: scale(0);
      }
  
      .slider-img{
        animation-name: loadPicture;
        animation-delay: 0s;
        animation-duration: 2s;
        animation-fill-mode: forwards;
      }
    }
  }

  @keyframes loadTitle{
    from{bottom: -40px; opacity: 0;}
    to{bottom: 0; opacity: 1;}
  }

  @keyframes loadInfos{
    from{bottom: -40px; opacity: 0;}
    to{bottom: 0; opacity: 1;}
  }

  @keyframes loadButton{
    from{transform: scale(0);}
    to{transform: scale(1);}
  }

  @keyframes loadPicture {
    from{transform: translate(-50%, -50%) scale(0);}
    to{transform: translate(-50%, -50%) scale(1);}
  }
</style>