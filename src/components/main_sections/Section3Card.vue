<template>
  <div class="section3card">
    <div class="pointer">
      <img :src="require(`@/assets/img/${cardInfo.img}`)" alt="example" class="rounded rounded-3 w-100">
      <div class="layover rounded rounded-3 d-flex flex-column justify-content-end ps-5 text-white pb-5">
        <div class="text-capitalize fs-3 fw-bold">
          {{cardInfo.title}} 
        </div>
        <div class="text-uppercase">
          {{cardInfo.desc}}
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name : 'Section3Card',
  props : {
    cardInfo : Object
  }
}
</script>


<style lang="scss">
  .section3card{
    position: relative;
    transition: all 1s;

    &:hover{
      transform: scale(1.1);
      z-index: 9;
    }

    &:hover .layover{
      visibility: visible;
    }

    .layover{
      z-index: 99;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
      visibility: hidden;
    }
  }
</style>