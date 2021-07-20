<template>
  <div class="chat">
    <div class="openChatBtn pointer"> <i class="far fa-comment"></i> </div>

  </div>
</template>

<script>
export default {
  name : 'Chat'
}
</script>

<style lang="scss">
  .chat{
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 9999;

    .openChatBtn{
      color: white;
      font-size: 2rem;
      font-weight: 700;
      background-color: #527ceb;
      padding: 10px 20px;
      border-radius: 50%;
      box-shadow: 2px 2px 3px rgba(128, 128, 128, 0.5);
      transition: all 0.3s;

      &:hover{
        background-color: #6a9fe4;
      }
    }
  }
</style>