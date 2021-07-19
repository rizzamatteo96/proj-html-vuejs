<template>
  <div class="slider position-relative">
    <div class="container-fluid m-0 px-0">

      <VueSlickCarousel 
      v-bind="settings"
      @afterChange="loadnumber"
      ref="carousel"
      >
        <!-- richiamo la card per visualizzare i risultati -->
        <SliderCard
        v-for="(card,i) in cardInfo" :key="i"
        :cardInfomations="card"
        />
      </VueSlickCarousel>

      <!-- richiamo la card per visualizzare i risultati
      <SliderCard
      :cardInfomations="cardInfo[index]"
      /> -->

      <div class="counter-slider">
        <ul>
          <li 
          v-for="(counter,i) in cardInfo" 
          :key="i"
          @click="goToSlideNr(i)"
          role="button"
          :class="(index == i) ? 'active' : ''"> 
          <span v-if="i < 10">0</span>{{i}}</li>
        </ul>
      </div>

    </div>
  </div>
</template>


<script>
import SliderCard from './SliderCard.vue'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'

export default {
  name : 'Slider',
  components : {
    SliderCard,
    VueSlickCarousel
  },
  data(){
    return{
      index : 0,
      settings : {
        accessibility : true,
        adaptiveHeight : false,
        arrows : false,
        asNavFor : null,
        autoplay : true,
        autoplaySpeed : 5000,
        centerMode : false,
        centerPadding : '50px',
        cssEase : 'ease',
        dots : false,
        dotsClass : 'slick-dots',
        draggable : true,
        edgeFriction : 0.35,
        fade : false,
        focusOnSelect : false,
        infinite : true,
        initialSlide : 0,
        lazyLoad : 'ondemand',
        pauseOnDotsHover : false,
        pauseOnFocus : false,
        pauseOnHover : true,
        responsive : null,
        rows : 1,
        rtl : false,
        slidesPerRow : 1,
        slidesToScroll : 1,
        slidesToShow : 1,
        speed : 500,
        swipe : true,
        swipeToSlide : true,
        touchMove : true,
        touchThreshold : 5,
        useCSS : true,
        useTransform : true,
        variableWidth : false,
        vertical : false,
        waitForAnimate : true,
      },
      cardInfo : [
        {
          mainTitleTop : 'We Are a',
          mainTitleBot : 'Web Design',
          mainTitleGreen : 'Agency',
          paragraf : 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.',
          img : require('../assets/img/slider-img-1.png')
        },
        {
          mainTitle : 'Cose2',
          mainTitleGreen : 'altre cose2',
          paragraf : 'blablablablabla2',
          img : require('../assets/img/slider-img-2.png')
        },
        {
          mainTitle : 'Cose3',
          mainTitleGreen : 'altre cose3',
          paragraf : 'blablablablabla3',
          img : require('../assets/img/slider-img-3.png')
        }
      ]
    }
  },
  methods : {
    loadnumber(loadedSlide){
      this.index = loadedSlide;
    },
    goToSlideNr(i){
      this.$refs.carousel.goTo(i)
    }
  }
}
</script>


<style lang="scss">
  @import '@/style/slider.scss';
</style>