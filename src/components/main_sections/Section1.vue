<template>
  <div>
    <div class="container-fluid">
      <div class="row my-5 g-0 align-items-center">
        <!-- inizio parte sinistra -->
        <div class="col-5 px-4">
          <div class="text-capitalize fw-bold fs-1">
            We are here to make your <span class="ms-green">website</span> look more <span class="ms-green">elegant</span> and stylish!
          </div>
          <div class="divider my-5"></div>
          <button class="ms-btn ms-btn-light-green">View all</button>
        </div>
        <!-- fine parte sinistra -->

        <!-- inizio parte destra -->
        <div class="col-7">
          <div class="find-out row row-cols-2 g-5 m-0 p-0">
            <div v-for="(data,i) in findOutData" :key="i">
              <div class="card p-5">
                <i :class="data.icon" class="mb-4 fs-1"></i>
                <div class="title fs-3 mb-2"> {{data.title}} </div>
                <div> {{data.par}} </div>
              </div>
            </div>
          </div>
        </div>
        <!-- fine parte destra -->
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name : 'Section1',
  data(){
    return{
      findOutData : [
        {
          icon : 'fas fa-tachometer-alt',
          title : 'Speed optimization',
          par : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-cloud',
          title : 'Cloud solution',
          par : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-mobile-alt',
          title : 'Website design',
          par : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
        {
          icon : 'fas fa-stopwatch',
          title : 'Online marketing',
          par : 'Far far away, behind the word mountains, far from countries Vokalia Separated...'
        },
      ]
    }
  }
}
</script>


<style lang="scss">
  .find-out .card {
    box-shadow: 0 0 30px lightgray;
    border-radius: 20px;
    transition: all 0.5s;
    i{
      transition: all 0.5s;
      color: #00d9a6;
    }

    &:hover{
      // background-color: red;
      background-image: linear-gradient(to right, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
      box-shadow: 5px 5px 20px  #00d9a656;
      color: white !important;
      cursor: pointer;

      i{
        color: white;
      }
    }
  }
</style>