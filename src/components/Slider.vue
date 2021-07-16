<template>
  <div class="slider position-relative">
    <div class="container h-100">

      <!-- richiamo la card per visualizzare i risultati -->
      <Card
      :cardInfomations="cardInfo[index]"
      />

      <div class="counter-slider">
        <ul>
          <li 
          v-for="(counter,i) in cardInfo" 
          :key="i"
          @click="index = i"
          role="button"
          :class="(index == i) ? 'active' : ''"> 
          <span v-if="i < 10">0</span>{{i}}</li>
        </ul>
      </div>

    </div>
  </div>
</template>


<script>
import Card from './Card.vue'

export default {
  name : 'Slider',
  components : {
    Card
  },
  data(){
    return{
      index : 0,
      cardInfo : [
        {
          mainTitleTop : 'We Are a',
          mainTitleBot : 'Web Design',
          mainTitleGreen : 'Agency',
          paragraf : 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.',
          img : 'slider-img-1.png'
        },
        {
          mainTitle : 'Cose2',
          mainTitleGreen : 'altre cose2',
          paragraf : 'blablablablabla2',
          img : 'slider-img-2.png'
        },
        {
          mainTitle : 'Cose3',
          mainTitleGreen : 'altre cose3',
          paragraf : 'blablablablabla3',
          img : 'slider-img-3.png'
        }
      ]
    }
  }
}
</script>


<style lang="scss">
  @import '@/style/slider.scss';
</style>