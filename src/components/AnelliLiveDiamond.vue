<template>
  <div class="block text-center anelli-title" data-aos="fade-down">
    <Typography :heading="1">Anelli</Typography>
    <Typography :heading="2">&nbsp;Live diamond</Typography>
  </div>
  <div class="block text-center anelli-text" data-aos="fade-down">
    <Text>
      <strong>Oro bianco e diamanti</strong> nei modelli più amati di sempre per celebrare i vostri momenti speciali.
      <strong>Solitari, trilogy ed eternity</strong> in diverse carature per accompagnare gli attimi di una vita
      insieme.
    </Text>
  </div>
  <div class="anelli-content">
    <div class="anelli-content__images">
      <picture class="anelli-content__image">
        <source
            media="(max-width: 768px)" width="445" height="691"
            srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/verticale_3_PNNOISoWp.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439404">
        <v-lazy-image
            class="img-cover" alt="Anelli - Live Diamond" width="950" height="1170"
            data-aos="zoom-out-up"
            data-aos-offset=""
            data-aos-delay=""
            data-aos-duration="500"
            data-aos-easing="linear"
            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/verticali_3_4ccmU1EzJ.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659348750265"/>
      </picture>
      <picture class="anelli-content__image">
        <source
            media="(max-width: 768px)" width="445" height="691"
            srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/verticale_4_6up_t7jEp.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439228">
        <v-lazy-image
            class="img-cover" alt="Anelli - Live Diamond" width="950" height="1170"
            data-aos="zoom-out-up"
            data-aos-offset=""
            data-aos-delay=""
            data-aos-duration="500"
            data-aos-easing="linear"
            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/verticali_4_CRVZQ_GsA.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659348750438"/>
      </picture>
    </div>
  </div>
  <div class="anelli-carousel">
    <CarouselVue :slide="slides"></CarouselVue>
  </div>
  <div class="text-center anelli__link" data-aos="fade-down">
    <Link :link="linkButton">Collezioni anelli</Link>
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

const linkButton = 'https://www.bluespirit.com/anelli-live-diamond-C5B222.htm';

const slides = [
  {
    title: 'Live Diamond - Anelli 1',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld01503012-P73411.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD01503012_ANELLI_FO0vnD4KJ.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729378'
  },
  {
    title: 'Live Diamond - Anelli 2',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld00504010-P73402.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD00504010_ANELLI_Z0gTebQ3v.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729584'
  },
  {
    title: 'Live Diamond - Anelli 3',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld05036010i-P79762.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD05036010I_ANELLI_ae9uwiihR.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729462'
  }
];

onMounted(() => {
  AOS.init();
});

</script>

<style scoped lang="scss">
.anelli-title {
  margin-bottom: 40px;
}

.text-center {
  text-align: center;
}

.anelli-text {
  max-width: 1088px;
  width: 100%;
  margin: 0 auto 40px;
}

.anelli-content {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 97%;
  margin-bottom: 40px;
}

.anelli-content__images {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.anelli-content__image {
  height: 0;
  padding-bottom: 70%;
  width: 58%;
  position: absolute;

  &:first-child {
    top: 0;
    left: 0;
    z-index: 2;
  }

  &:last-child {
    right: 0;
    z-index: 1;
    bottom: 0%;
  }
}

.img-cover {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.anelli-carousel {
  width: 100%;
  max-width: 30%;
  display: block;
  border: 2px solid #215732;
  margin-left: 18%;
  margin-top: -20%;
  margin-bottom: 40px;
  z-index: 3;
  position: relative;
}

.anelli__link{
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
  .anelli__link{
    margin-bottom: 70px;
  }
  .anelli-content {
    padding-bottom: 115%;
  }
  .anelli-content__image {
    padding-bottom: 73%;
  }
  .anelli-carousel{
    max-width: 50%;
    margin-left: 10%;
    margin-top: -30%;
  }
}
</style>