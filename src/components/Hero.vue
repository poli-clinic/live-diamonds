<template>
  <picture class="hero"
       data-aos="zoom-out-up"
       data-aos-delay="0"
       data-aos-duration="400"
       data-aos-easing="linear"
  >
    <source
        media="(max-width: 768px)"
        srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/slider_1_6Jq1cpeZn.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439316">
    <img
        alt="Landing page - Live Diamond"
        width="1633"
        height="633"
        class="img-cover"
        src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/ld_slider_1_1tA79JoFP.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659101601692">
  </picture>
  <div class="hero__title" data-aos="fade-down">
    <div class="block text-center">
      <Typography :heading="1">Il Diamante</Typography>
    </div>
    <div class="block text-center">
      <Typography :heading="2">che ama il pianeta</Typography>
    </div>
  </div>

  <div class="text text-center" data-aos="fade-down">
    <Text>
      <strong>Live Diamond</strong> è il brand italiano di diamanti accresciuti in laboratorio, <strong>ecologici e
      socialmente compatibili</strong>. Ogni diamante viene realizzato attraverso un processo all’avanguardia che dà
      vita a pietre di grande qualità ma senza estrarle dal suolo, limitando i danni per <strong>l’ambiente</strong>.
    </Text>
  </div>

  <div class="text-center hero__link" data-aos="fade-down">
    <Link :link="linkButton">Scopri live diamond</Link>
  </div>

</template>

<script setup>
import {onMounted} from "@vue/runtime-core";
import Typography from "./Typography.vue";
import Text from "./Text.vue";
import Link from "./Link.vue";
import AOS from 'aos';
import 'aos/dist/aos.css'

const linkButton = 'https://www.bluespirit.com/live-diamond-B222.htm';

onMounted(() => {
  AOS.init();
});
</script>

<style scoped lang="scss">
.hero {
  height: 0;
  padding-bottom: 39%;
  width: 100%;
  overflow: hidden;
  margin-bottom: 56px;
  display: block;
}

.img-cover {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.text-center {
  text-align: center;
}

.block {
  display: block;
}

.text {
  display: block;
  margin: 0 auto;
  width: 100%;
  max-width: 1088px;
}
.hero__title{
  margin-bottom: 40px;
}
.hero__link{
  margin-bottom: 100px;
}

.show-mobile{
  display: none;
}

@media (max-width: 768px){
  .hidden-mobile{
    display: none;
  }
  .show-mobile{
    display: block;
  }
  .hero__link{
    margin-bottom: 70px;
  }
  .hero {
    padding-bottom: 118%;
  }
}
</style>