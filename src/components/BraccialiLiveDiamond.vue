<template>
  <div class="bracciali">
    <div class="bracciali__1">
      <Typography :heading="2" data-aos="zoom-in"
                  data-aos-offset="300px"
                  data-aos-delay="100"
                  data-aos-duration="400"
                  data-aos-easing="linear">
        Bracciali live Diamond
      </Typography>
      <div class="bracciali__content">
        <div
            data-aos="zoom-in"
            data-aos-offset="300px"
            data-aos-delay="300"
            data-aos-duration="400"
            data-aos-easing="linear"
        >
          <Text>
            I bracciali LIVE DIAMOND, per versatilità ed eleganza, sono perfetti come idea regalo che possa durare nel
            tempo. Da soli o nel multindosso donano lucentezza ad ogni look.
          </Text>
        </div>

        <div class="bracciali-carousel mb-2">
          <CarouselVue :slide="slides"></CarouselVue>
        </div>
        <div class="text-center"
             data-aos="zoom-in"
             data-aos-offset="300px"
             data-aos-delay="100"
             data-aos-duration="400"
             data-aos-easing="linear"
        >
          <Link :link="linkButton">
            Collezioni bracciali
          </Link>
        </div>
      </div>
    </div>
    <div class="bracciali__image"
         data-aos="zoom-out-up"
         data-aos-offset="300px"
         data-aos-delay="200"
         data-aos-duration="400"
         data-aos-easing="linear"
    >
      <v-lazy-image alt="Bracciali - Live Diamond" width="531" height="665"
          src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/bracciali_WGxLpRosy.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658752425564"
          class="block w-100" />
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

const linkButton = 'https://www.bluespirit.com/bracciali-live-diamond-C16B222.htm';

const slides = [
  {
    title: 'Live Diamond - Bracciali 1',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld05615-P73434.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bracciali_1_y3bcBdeQFD.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412590'
  },
  {
    title: 'Live Diamond - Bracciali 2',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld71439i-P79828.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bracciali_2_fk515P02I.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755413546'
  },
  {
    title: 'Live Diamond - Bracciali 3',
    link: 'https://www.bluespirit.com/bracciale-live-diamond-live-diamond-ld851041i-P79935.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bracciali_3_PhDycRq6R.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412547'
  }
];

onMounted(() => {
  AOS.init();
});

</script>

<style scoped lang="scss">
.bracciali {
  padding-left: 10%;
  padding-right: 20%;
  display: flex;
  align-items: flex-start;
  margin-bottom: 5rem;
  position: relative;
}

.bracciali__1 {
  flex: 0 1 60%;
  max-width: 60%;
  padding: 0 15px;
  position: relative;
  z-index: 2;
}

.bracciali-carousel {
  width: 100%;
  max-width: 380px;
  display: block;
  margin: 0 auto;
  border: 2px solid #215732;
}

.mb-2 {
  margin-bottom: 2rem;
}

.text-center {
  text-align: center;
}

.bracciali__image {
  flex: 0 1 40%;
  max-width: 40%;
  padding: 0 15px;
  position: relative;

  img {
    position: absolute;
    right: 0;
    width: 130%;
    height: auto;
  }
}

.block {
  display: block;
}

.bracciali__content {
  padding-right: 190px;
}

@media (max-width: 1300px){
  .bracciali{
    padding: 0 15px;
  }
  .bracciali__content {
    padding-right: 0px;
  }

  .bracciali__image img {
    width: 100%;
    position: relative;
  }
}

@media (max-width: 767px){
  .bracciali {
    flex-wrap: wrap;
  }
  .bracciali__1 {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0;
    margin-bottom: 3rem;
  }
  .bracciali__image {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0px;
  }
}

</style>