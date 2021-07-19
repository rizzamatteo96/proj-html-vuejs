<template>
  <div class="section4 my-5 ">
    <div class="container-fluid overlay text-center py-5">
      <div class="ms-fs-big ms-green">“</div>
      <div class="text-secondary fst-italic fs-4 my-5 w-50 mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos odit natus expedita nulla iure ut numquam repellat veritatis saepe cumque odio repellendus nihil unde sint nemo nobis, voluptate iusto consequuntur!</div>
      <div class="client"> 
        <img src="@/assets/img/business-woman.jpg" alt="business woman">
        <div class="text-uppercase ms-green fs-5">Lissa Dublin</div>
        <div class="text-secondary">Client</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name : 'Section3'
}
</script>

<style lang="scss">
  .section4{
    background-image: url('../../assets/img/four-businesspeople.jpg');
    background-size: cover;
    background-position: center;

    .overlay{
      background-image: linear-gradient(to left, rgba(54, 54, 54, 0.8) , rgba(0, 0, 0, 0.8));
    }

    .ms-fs-big{
      font-size: 8rem;
    }

    .client img{
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
    }
  }
</style>