<template>
  <div class="chat">
    <!-- inizio gestione pulsante apertura / chiusura chat -->
    <div class="openChatBtn pointer" @click="chatOpen = !chatOpen"> 
      <i class="far fa-comment" v-if="!chatOpen"></i> 
      <i class="fas fa-times" v-if="chatOpen"></i>
    </div>
    <!-- fine gestione pulsante apertura / chiusura chat -->


    <!-- inizio contenitore della chat -->
    <div class="chatBox" v-if="chatOpen">
      <div class="top">
        <button class="active"><i class="far fa-comment"></i> Ask</button>
        <button><i class="fas fa-search"></i> FAQ</button>
        <div class="avatar-sec">
          <img v-for="(img,i) in 5" :key="i" src="@/assets/img/avatar-chat.png" alt="avatar">
        </div>
        <div class="title">How can we help?</div>
        <div class="par">We usually respond in a few hours</div>

      </div>
      <div class="main">
        <label for="name">Name</label>
        <input type="text" id="name">
        
        <label for="subject">Subject</label>
        <input type="text" id="subject">
        
        <label for="email">Email address</label>
        <input type="text" id="email">
        
        <label for="how">How can we help?</label>
        <input type="text" id="how">

        <button class="send pointer">Send a message</button>
      </div>

    </div>
    <!-- fine contenitore della chat -->

  </div>
</template>

<script>
export default {
  name : 'Chat',
  data(){
    return{
      chatOpen : false
    }
  }
}
</script>

<style lang="scss">
  .chat{
    position: fixed;
    bottom: 20px;
    right: 50px;
    z-index: 9999;

    .openChatBtn{
      color: white;
      font-size: 2rem;
      font-weight: 700;
      background-color: #527ceb;
      height: 60px;
      width: 60px;
      border-radius: 50%;
      box-shadow: 2px 2px 3px rgba(128, 128, 128, 0.5);
      transition: all 0.3s;
      text-align: center;
      line-height: 60px;

      i{
        animation-name: loadIcon;
        animation-duration: 0.5s;
        animation-fill-mode: forwards;
        transform: scale(0);
      }

      &:hover{
        background-color: #3063ec;
      }
    }

    .chatBox{
      position: absolute;
      right: 0px;
      bottom: 80px;
      width: 20vw;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 5px 5px 10px grey;

      .top{
        background-color: #527ceb;
        // height: 30%;
        border-radius: 10px 10px 0 0;
        padding: 20px;
        text-align: center;

        button{
          background-color: unset;
          border: none;
          border-radius: 30px;
          padding: 5px 20px;
          color: white;

          &.active{
            background-color: rgba(0, 0, 0, 0.3);
            font-weight: bold;
          }
        }

        .avatar-sec{
          padding: 3% 0;
          
          img{
            height: 50px;
            width: 50px;
            border-radius: 50%;
            border: 1px solid white;
            object-fit: cover;
            margin: 0 2px;
          }
        }

        .title{
          color: white;
        }

        .par{
          color: rgba(255, 255, 255, 0.8);
        }
      }

      .main{
        padding: 20px;

        label{
          display: block;
          color: grey;
          margin-bottom: 5px;
        }

        input{
          width: 100%;
          padding: 5px 10px;
          border: 1px solid lightgrey;
          border-radius: 5px;
          margin-bottom: 10px;
        
          &#how{
            padding: 5px 10px 50px;
          }
        }


        .send{
          text-align: center;
          color: white;
          background-color: #527ceb;
          width: 100%;
          border: none;
          border-radius: 5px;
          padding: 15px 0;

          &:hover{
            background-color: #3063ec;
          }
        }
      }
    }
  }

  @keyframes loadIcon {
    from{transform: scale(0);}
    to{transform: scale(1);}
  }
</style>