<template>
  <BannerContainer />
  <JogosContainer />
  <FooterContainer />
</template>

<script>
  import BannerContainer from './components/BannerContainer.vue';
  import JogosContainer from './components/JogosContainer.vue';
  import FooterContainer from './components/FooterContainer.vue';
  export default{
      components:{
        BannerContainer,
        JogosContainer,
        FooterContainer,
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
    list-style: none;
  }
</style>