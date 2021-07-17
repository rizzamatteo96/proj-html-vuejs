<template>
  <main>

    <!-- Caricamento componente slider -->
    <Slider/>

    <!-- Caricamento prima sezione -->
    <Section1/>

    <!-- Caricamento della seconda sezione -->
    <Section2/>

  </main>
</template>


<script>
import Slider from './Slider.vue'
import Section1 from './main_sections/Section1.vue'
import Section2 from './main_sections/Section2.vue'

export default {
  name : 'Main',
  components : {
    Slider,
    Section1,
    Section2,
  }
}
</script>


<style lang="scss">

</style>