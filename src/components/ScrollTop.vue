<template>
  <div :class="(!enable) ? 'd-none' : 'd-block'" class="scroll-top pointer" @click="scrollTop">
    <i class="fas fa-arrow-up"></i>
  </div>
</template>

<script>
export default {
  name : "ScrollTop",
  props : {
    enable : Boolean
  },
  methods : {
    scrollTop(){
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    }
  }
}
</script>

<style lang="scss">
  .scroll-top{
    position: fixed;
    bottom: -30px;
    right: 130px;
    z-index: 9999;
    background-color: white;
    padding: 10px 15px;
    border: 1px solid black;
    border-radius: 50%;
    transition: all 0.5s;
    animation-name: appearScroll;
    animation-duration: 0.3s;
    animation-fill-mode: forwards;
    animation-timing-function: ease-in-out;

    &:hover{
      background-color: black;
      border: 1px solid white;
      color: white;
    }

    @keyframes appearScroll {
      from{bottom: -30px;}
      to{bottom: 25px;}
    }
  }
</style>