<template>
  <div class="block text-center bracciali-title" data-aos="fade-down">
    <Typography :heading="1">Bracciali</Typography>
    <Typography :heading="2">&nbsp;Live diamond</Typography>
  </div>
  <div class="block text-center bracciali-text" data-aos="fade-down">
    <Text>
      <strong>I bracciali LIVE DIAMOND</strong> sono perfetti come idea regalo che possa durare nel tempo.<br> Da
      <strong>soli</strong> o nel <strong>multi indosso</strong> donano lucentezza ad ogni look.
      insieme.
    </Text>
  </div>
  <div class="bracciali-content">
    <div class="bracciali-content__image">
      <picture class="bracciali-image">
        <source
            media="(max-width: 768px)" width="445" height="691"
            srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/verticale_5_McAq42UlH.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439264">
        <v-lazy-image
            class="img-cover" alt="Anelli - Live Diamond" width="950" height="1170"
            data-aos="zoom-out-up"
            data-aos-offset=""
            data-aos-delay=""
            data-aos-duration="500"
            data-aos-easing="linear"
            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/verticali_5_lcw7YNeMZ.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659351175879"/>
      </picture>
    </div>
    <div class="bracciali-content__carousel">
      <div class="bracciali-carousel">
        <CarouselVue :slide="slides"></CarouselVue>
      </div>
    </div>
  </div>
  <div class="text-center bracciali__link" data-aos="fade-down">
    <Link :link="linkButton">Collezioni bracciali</Link>
  </div>
</template>

<script setup>
import {onMounted} from "@vue/runtime-core";
import CarouselVue from "./Carousel.vue";
import Typography from "./Typography.vue";
import Text from "./Text.vue";
import Link from "./Link.vue";
import VLazyImage from "v-lazy-image";
import AOS from 'aos';
import 'aos/dist/aos.css'

const linkButton = 'https://www.bluespirit.com/bracciali-live-diamond-C16B222.htm';

const slides = [
  {
    title: 'Live Diamond - Bracciali 1',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld05615-P73434.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD05615_BRACCIALI_82tiG9zCbS.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365730317'
  },
  {
    title: 'Live Diamond - Bracciali 2',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld71439i-P79828.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD71439I_BRACCIALI_t3O8W7BxWJ.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729314'
  },
  {
    title: 'Live Diamond - Bracciali 3',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld851041i-P79935.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD851041I_BRACCIALI_iTWu51456.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729213'
  }
];

onMounted(() => {
  AOS.init({once: true, mirror: false});
});

</script>

<style scoped lang="scss">
.bracciali-title {
  margin-bottom: 40px;
}

.text-center {
  text-align: center;
}

.bracciali-text {
  max-width: 1088px;
  width: 100%;
  margin: 0 auto 40px;
}

.bracciali-content{
  display: flex;
  margin-left: -8px;
  margin-right: -8px;
  flex-wrap: wrap;
  margin-bottom: 40px;
  align-items: center;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
}

.bracciali-content__image{
  flex: 0 0 58%;
  max-width: 58%;
  padding: 0 8px;
  position: relative;
  z-index: 2;
}

.bracciali-content__carousel{
  flex: 0 0 42%;
  max-width: 42%;
  padding: 0 8px;
  position: relative;
  z-index: 1;
}

.bracciali-image{
  width: 100%;
  position: relative;
  padding-bottom: 115%;
  display: block;
}

.img-cover {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.bracciali-carousel {
  display: block;
  border: 2px solid #215732;
  margin: 0 auto;
  max-width: 530px;
  width: 100%;
}

.bracciali__link{
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
  .bracciali__link{
    margin-bottom: 70px;
  }
  .bracciali-content__image {
    flex: 0 0 75%;
    max-width: 75%;
  }
  .bracciali-image{
    padding-bottom: 140%;
  }
  .bracciali-content{
    position: relative;
  }
  .bracciali-content__carousel {
    max-width: 50%;
    padding: 0;
    z-index: 2;
    position: absolute;
    right: 15px;
    bottom: 25px;
    width: 100%;
  }
}
</style>