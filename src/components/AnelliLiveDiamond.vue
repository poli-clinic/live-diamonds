<template>
  <div class="anelli">
    <div class="anelli__1">
      <div class="anelli-content"
           data-aos="zoom-in"
           data-aos-offset="300px"
           data-aos-delay="100"
           data-aos-duration="400"
           data-aos-easing="linear"
      >
        <Typography :heading="2">
          Anelli live Diamond
        </Typography>
        <Text>
          Oro bianco e diamanti nei modelli più amati di sempre per celebrare i vostri momenti speciali. Solitari,
          trilogy ed eternity in diverse carature per accompagnare gli attimi di una vita insieme.
        </Text>
      </div>
      <v-lazy-image alt="Anelli - Live Diamond" width="828" height="531"
          data-aos="zoom-out-up"
          data-aos-offset="300px"
          data-aos-delay="300"
          data-aos-duration="400"
          data-aos-easing="linear"
          src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/anelli_1_yHutgSNL7.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658751508982"
          class="w-100 block anelli-image" />
      <div class="text-center"
           data-aos="zoom-in"
           data-aos-offset="300px"
           data-aos-delay=""
           data-aos-duration="400"
           data-aos-easing="linear"
      >
        <Link :link="linkButton">
          acquista i best seller
        </Link>
      </div>
    </div>
    <div class="anelli__2">
      <v-lazy-image alt="Anelli - Live Diamond" width="552" height="552"
          data-aos="zoom-out-up"
          data-aos-offset="300px"
          data-aos-delay="200"
          data-aos-duration="400"
          data-aos-easing="linear"
          src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/anelli_2_yPuSNj8un.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658751509036"
          class="w-100 block mb-2" />
      <div class="anelli-carousel mb-2">
        <CarouselVue :slide="slides"></CarouselVue>
      </div>
    </div>
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
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/anelli_1_U1vPJrMDh.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412498'
  },
  {
    title: 'Live Diamond - Anelli 2',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld00504010-P73402.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/anelli_2_Ihyqohx7z.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412511'
  },
  {
    title: 'Live Diamond - Anelli 3',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld05036010i-P79762.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/anelli_3_gMotPNN393.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755414913'
  }
];

onMounted(() => {
  AOS.init();
});

</script>

<style scoped>
.anelli {
  padding-left: 0px;
  padding-right: 0px;
  display: flex;
  align-items: flex-start;
  margin-bottom: 5rem;
  position: relative;
  width: 100%;
}

.anelli__1 {
  flex: 0 1 60%;
  max-width: 60%;
  padding: 0 15px;
}

.w-100 {
  width: 100%;
  height: auto;
}

.block {
  display: block;
}

.mb-2 {
  margin-bottom: 2rem;
}

.anelli-content {
  padding-left: 80px;
}

.anelli__2 {
  flex: 0 1 40%;
  max-width: 40%;
  padding: 0 15px;
}

.anelli-carousel{
  width: 100%;
  max-width: 380px;
  display: block;
  margin: 0 auto;
  border: 2px solid #215732;
}

.anelli-image{
  margin-bottom: 4rem;
}

.text-center{
  text-align: center;
}

@media (max-width: 767px) {
  .anelli {
    flex-wrap: wrap;
  }
  .anelli__1 {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0px;
    margin-bottom: 5rem;
  }

  .anelli__2 {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0px;
  }

  .anelli-content {
    padding-left: 0px;
  }
}

</style>