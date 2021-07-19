<template>
  <div class="section4">
    <div class="container-fluid overlay text-center py-5">
      <div class="ms-fs-big ms-green">“</div>
      <div class="text-secondary fst-italic fs-4 my-5 w-50 mx-auto">When it comes to barbequing, there are two main schools of thought for the techniques that you can use. Freshly scrambled eggs with applewood smoked bacon - are amazing!</div>
      <div class="client"> 
        <img src="@/assets/img/business-woman.jpg" alt="business woman" class="mb-3">
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
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 5px solid white;
      object-fit: cover;
    }
  }
</style>