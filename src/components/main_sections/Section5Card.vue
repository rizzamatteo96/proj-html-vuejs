<template>
  <div class="section5-card">
    <div class="ms-container w-100 position-relative">
      <img 
      :src="require(`@/assets/img/${cardData.img}`)" 
      alt="business picture"
      class="w-100">

      <div class="test text-start">
        <div class="text-secondary fs-6"> {{cardData.date}} </div>
        <ul class="p-0 fs-4 fw-bold">
          <li> {{cardData.title}} </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name :'Section5Card',
  props : {
    'cardData' : Object
  }
}
</script>

<style lang="scss">
  .section5-card{
    img{
      box-shadow: 5px 5px 20px grey;
      border-radius: 5px;
    }

    .test{
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 50%);

      padding: 3rem 0 1rem 3rem;

      background-color: #fff;
      border-radius: 5px;
      box-shadow: 5px 5px 20px grey;
      width: 80%;

      ul li::marker{
        color: #00d9a6;
      }
    }
  }
</style>