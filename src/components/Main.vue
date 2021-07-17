<template>
  <main>

    <!-- Caricamento componente slider -->
    <Slider/>

    <!-- Caricamento prima sezione -->
    <Section1/>

    <!-- Caricamento della seconda sezione -->
    <Section2/>

    <!-- Caricamento della terza sezione -->
    <Section3/>

  </main>
</template>


<script>
import Slider from './Slider.vue'
import Section1 from './main_sections/Section1.vue'
import Section2 from './main_sections/Section2.vue'
import Section3 from './main_sections/Section3.vue'

export default {
  name : 'Main',
  components : {
    Slider,
    Section1,
    Section2,
    Section3,
  }
}
</script>


<style lang="scss">

</style>