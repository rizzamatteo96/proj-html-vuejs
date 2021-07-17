<template>
  <main>

    <!-- Caricamento componente slider -->
    <Slider/>

    <!-- Caricamento prima sezione -->
    <Section1/>

  </main>
</template>


<script>
import Slider from './Slider.vue'
import Section1 from './main_sections/Section1.vue'

export default {
  name : 'Main',
  components : {
    Slider,
    Section1
  }
}
</script>


<style lang="scss">

</style>