<template>
  <div class="section5 py-5">
    <div class="container-fluid text-center">
      <!-- titolo + divisore sezione -->
      <div class="title text-capitalize fs-1 fw-bold">Latest news &amp; our <span class="ms-green">blog</span></div>
      <div class="divider my-5"></div>

      <!-- inizio card con immagini -->
      <div class="row row-cols-3">
        <Section5Card v-for="(card,i) in cardsData" :key="i" :cardData="card"/>
      </div>
      <!-- fine card con immagini -->

      <!-- pulsante centrale nero -->
      <div class="text-center">
        <button class="ms-btn ms-btn-black btn-view">View all post</button>
      </div>

      <!-- inizio box colorate -->
      <div class="coloured-boxes text-white row row-cols-2 mb-5">
        <!-- inizio box sinistra -->
        <div>
          <div class="left">
            <div class="text-secondary">Are you ready?</div>
            <div class="fs-1 fw-bold">Start a New Project</div>
            <div class="insert-mail mt-5">
              <input type="text" placeholder="Enter Your Email Address">
              <button>Submit</button>
            </div>
          </div>
        </div>
        <!-- fine box sinistra -->

        <!-- inizio box destra -->
        <div>
          <div class="right">
            <div class="text-secondary">What Are you Waiting for?</div>
            <div class="fs-1 fw-bold">Let's talk about work</div>
            <button class="ms-btn ms-btn-black mt-5 text-uppercase">Start now</button>
          </div>
        </div>
        <!-- fine box destra -->
      </div>
      <!-- fine box colorate -->

      <!-- inizio sezione sponsor -->
      <div class="sponsor row row-cols-6 align-items-center my-5">
        <div v-for="(img,i) in 6" :key="i" >
          <img :src="require(`@/assets/img/client${i+1}.png`)" :alt="`client number ${i+1} picture`">
        </div>
      </div>
      <!-- fine sezione sponsor -->

    </div>
  </div>
</template>


<script>
import Section5Card from './Section5Card.vue'

export default {
  name : 'Section5',
  components : {
    Section5Card
  },
  data(){
    return{
      cardsData : [
        {
          img : 'sec5-1.jpg',
          date : 'May 24, 2018 - by Alex',
          title : 'Marketing ideas'
        },
        {
          img : 'sec5-2.jpg',
          date : 'May 24, 2018 - by Alex',
          title : 'Rest during working hours'
        },
        {
          img : 'sec5-3.jpg',
          date : 'May 24, 2018 - by Alex',
          title : 'develop your startup idea'
        },
      ]
    }
  }
}
</script>


<style lang="scss">
  .section5{
    background-color: #f9f9f9;

    .btn-view{
      margin: 10rem 0 5rem 0;
    }

    .coloured-boxes{

      .left,
      .right{
        border-radius: 20px;
        padding: 4rem 0;
        box-shadow: 5px 5px 20px grey;
      }

      .left{
        background-image: linear-gradient(to right, rgb(54, 54, 54) , black);

        .insert-mail{
          width: 70%;
          margin: 0 auto;
          background-color: grey;
          padding: 0 3rem;
          border: none;
          border-radius: 100px;

          input{
            padding: 1rem 15% 1rem 0;
            background-color: unset;
            border: none;
          }

          button{
            background-color: unset;
            border: none;
            text-transform: uppercase;
            color: #444444
          }
        }
      }

      .right{
        background-image: linear-gradient(to left, rgba(7, 217, 0, 0.8) , rgba(0, 219, 168, 0.8));
      }
    }
  }
</style>