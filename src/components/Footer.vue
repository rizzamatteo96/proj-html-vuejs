<template>
  <div class="footer">

    <!-- inizio footer top -->
    <div class="container-fluid">
      <div class="top row row-cols-4 my-5 py-5">

        <!-- inizio colonna 1 -->
        <div>
          <img src="@/assets/img/logo_big.png" alt="logo phlox" class="mb-3">
          <div>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Esse architecto suscipit incidunt nam hic quos rerum voluptatibus eum dignissimos et, accusantium cupiditate, repellendus ex corporis. Omnis voluptatem totam explicabo excepturi.</div>
        </div>
        <!-- fine colonna 1 -->

        <!-- inzio colonna 2 -->
        <div>
          <div class="title">Quick links</div>
          <div class="divider my-3"></div>
          <ul>
            <li v-for="(link,i) in quickLinks" :key="i">
              <a :href="link.link"> {{link.text}} </a>
            </li>
          </ul>
        </div>
        <!-- fine colonna 2 -->

        <!-- inizio colonna 3 -->
        <div>
          <div class="title">Contact</div>
          <div class="divider my-3"></div>
          <div>Patricia V. Amedee 4401 Waldeck Street Grepevine Nashville, TX 76051</div>
          <div class="my-3">info@yourdomain.com</div>
          <div>+99 (0) 101 0000 888</div>
        </div>
        <!-- fine colonna 3 -->

        <!-- inizio colonna 4 -->
        <div>
          <div class="title">Location on map</div>
          <div class="divider my-3"></div>
          <img src="@/assets/img/map.png" alt="map img" class="w-100">
        </div>
        <!-- fine colonna 4 -->

      </div>
    </div>
    <!-- fine footer top -->

    <!-- inizio footer bottom -->
    <div class="bottom d-flex justify-content-between align-items-center text-white px-5">
      <div class="left text-uppercase">
        &copy; 2020 Phlox business theme.
      </div>
      <div class="right">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-pinterest-p"></i>
      </div>
    </div>
    <!-- fine footer bottom -->

  </div>
</template>


<script>
export default {
  name : 'Footer',
  data(){
    return{
      quickLinks : [
        {
          text : 'Careers',
          link : '#'
        },
        {
          text : 'News',
          link : '#'
        },
        {
          text : 'Terms of use',
          link : '#'
        },
        {
          text : 'Privacy Project',
          link : '#'
        },
        {
          text : 'About',
          link : '#'
        },
        {
          text : 'Contact',
          link : '#'
        }
      ]
    }
  }
}
</script>


<style lang="scss">
  .footer{

    .top{

      & > *{
        padding: 2rem;
      }

      .title{
        text-transform: uppercase;
        font-size: 1.5rem;
        font-weight: bold;
      }

      ul{
        list-style: none;
        padding: 0;

        li a{
          text-decoration: none;
          color: black;

          &:hover{
            color: #00d9a6;
            cursor: pointer;
          }
        }
      }
    }

    .bottom{
      height: 100px;
      background-image: linear-gradient(to right, rgb(54, 54, 54) , black);

      .right > *{
        margin: 0 10px;
      }
    }
  }
</style>