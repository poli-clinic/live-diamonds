<template>
  <div id="live-diamond">
    <Hero></Hero>
    <LabGrown></LabGrown>
    <AnelliLiveDiamond></AnelliLiveDiamond>
    <BraccialiLiveDiamond></BraccialiLiveDiamond>
  </div>
</template>

<script setup>
import Hero from './components/Hero.vue'
import LabGrown from './components/LabGrown.vue'
import AnelliLiveDiamond from './components/AnelliLiveDiamond.vue'
import BraccialiLiveDiamond from './components/BraccialiLiveDiamond.vue'
</script>

<style scoped lang="scss">
#live-diamond {
  font-family: 'Montserrat', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  box-sizing: border-box;
  margin-top: 40px;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
  width: 100%;
  max-width: 1470px;
  overflow: hidden;
}

@media (max-width: 768px){
  #live-diamond {
    max-width: 600px;
    *{
      text-align: center;
    }
  }
}
</style>
