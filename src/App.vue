<template>
  <BannerContainer />
  <JogosContainer />
  
</template>

<script>
  import BannerContainer from './components/BannerContainer.vue';
  import JogosContainer from './components/JogosContainer.vue';
  export default{
      components:{
        BannerContainer,
        JogosContainer,
      }
  }
</script>

<style>
  *{
    margin:0;
    padding: 0;
    box-sizing: border-box;
    color:#fff;
    font-family: sans-serif;
    text-decoration: none;
  }
</style>