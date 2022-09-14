<template>
  <div id="live-diamond">
    <Hero></Hero>
    <LabGrown></LabGrown>
    <AnelliLiveDiamond></AnelliLiveDiamond>
    <BraccialiLiveDiamond></BraccialiLiveDiamond>
    <Footer></Footer>
  </div>
</template>

<script setup>
import Hero from './components/Hero.vue'
import LabGrown from './components/LabGrown.vue'
import AnelliLiveDiamond from './components/AnelliLiveDiamond.vue'
import BraccialiLiveDiamond from './components/BraccialiLiveDiamond.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped lang="scss">
#live-diamond {
  font-family: 'Montserrat', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  box-sizing: border-box;
  margin-top: 0px;
  padding-right: 0px;
  padding-left: 0px;
  margin-right: auto;
  margin-left: auto;
  width: 100%;
  max-width: 1240px;
  overflow: hidden;
  hyphens: none;
  word-wrap: unset;
  *{
    hyphens: none;
    word-wrap: unset;
  }
}

@media (max-width: 768px){
  #live-diamond {
    padding-right: 0px;
    padding-left: 0px;
  }
}
</style>
