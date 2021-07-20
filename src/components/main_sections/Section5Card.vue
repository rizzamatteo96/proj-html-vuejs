<template>
  <div class="section5-card">
    <div class="ms-container w-100 position-relative">
      <div class="img-cont">
        <img 
        :src="require(`@/assets/img/${cardData.img}`)" 
        alt="business picture"
        class="w-100">
      </div>

      <div class="text-place text-start">
        <div class="ms-text-secondary fs-6"> {{cardData.date}} </div>
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

    .img-cont{
      overflow: hidden;

      img{
        box-shadow: 5px 5px 20px grey;
        border-radius: 5px;
        transition: transform 1s;
      }
    }

    

    &:hover{
      .img-cont img{
        transform: scale(1.1);
      }

      .text-place{
        bottom: -20px;
        background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
        color: white;
  
        .ms-text-secondary{
          color: white;
        }
  
        ul li::marker{
          color: white;
        }
      }
    } 

    .text-place{
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 50%);

      padding: 3rem 0 1rem 3rem;

      background-color: #fff;
      border-radius: 5px;
      box-shadow: 5px 5px 20px grey;
      width: 80%;

      transition: bottom 1s, color 0.5s;

      .ms-text-secondary{
        color: grey;
      }

      ul li::marker{
        color: #00d9a6;
      }
    }
  }
</style>