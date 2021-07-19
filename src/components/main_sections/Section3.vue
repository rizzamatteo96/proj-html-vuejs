<template>
  <div class="section3">
    <div class="container-fluid my-5 py-5">

      <!-- inizio parte superiore sezione 3 -->
      <div class="row align-items-end top">
        <!-- inizio parte sinistra -->
        <div class="col-5">

          <div class="divider my-5"></div>

          <div class="title fs-1 fw-bold">
            Our recent <span class="ms-green">web design</span> &amp; some examples of past <span class="ms-green">projects</span>
          </div>

          <div class="divider my-5"></div>

        </div>
        <!-- fine parte sinistra -->

        <!-- inizio parte destra -->
        <div class="col-7">
          <div class="text-secondary mb-5">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque sunt quia placeat ipsa fuga molestiae, rem sint quibusdam vero voluptatem aut consectetur. Fuga maiores doloribus blanditiis iure ipsa illo delectus? Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nulla repellat impedit eveniet placeat debitis sit aliquid amet illum quibusdam ex quod totam temporibus, provident, atque eaque, dolores consequatur quas. Minima.
          </div>
        </div>
        <!-- fine parte destra -->
      </div>
      <!-- fine parte superiore sezione 3 -->

      <!-- inizio parte inferiore sezione 3 -->
      <div class="row row-cols-4 g-1 mb-5 bottom">
        <div v-for="(card,i) in cardData" :key="i">
          <Section3Card 
          :cardInfo="card"/>
        </div>
        <!-- <img v-for="(img,i) in 8" :key="i" :src="require(`@/assets/img/sec3-${i+1}.jpg`)" alt="example" class="rounded rounded-3"> -->
      </div>
      <!-- fine parte inferiore sezione 3 -->

      <!-- pulsante finale sezione 3 -->
      <div class="text-center">
        <button class="ms-btn ms-btn-light-green my-5">Read more</button>
      </div>

    </div>
  </div>
</template>

<script>
import Section3Card from './Section3Card'

export default {
  name : 'Section3',
  components : {
    Section3Card
  },
  data(){
    return{
      cardData : [
        {
          img : 'sec3-1.jpg',
          title : 'The basket of flowers',
          desc : ' Branding - marketing '
        },
        {
          img : 'sec3-2.jpg',
          title : 'A famous ferris wheel ',
          desc : 'Marketing'
        },
        {
          img : 'sec3-3.jpg',
          title : 'Complementary colors ',
          desc : 'Branding - Marketing'
        },
        {
          img : 'sec3-4.jpg',
          title : 'Business prestige ',
          desc : 'Branding'
        },
        {
          img : 'sec3-5.jpg',
          title : 'Colorful origami boats',
          desc : 'Branding - Marketing'
        },
        {
          img : 'sec3-6.jpg',
          title : 'Modern Couch ',
          desc : 'Marketing'
        },
        {
          img : 'sec3-7.jpg',
          title : 'Hot air balloons ',
          desc : 'Branding - Marketing'
        },
        {
          img : 'sec3-8.jpg',
          title : 'Make Difference',
          desc : 'Branding'
        },
      ]
    }
  }
}
</script>

<style lang="scss">

</style>