<template>
  <div class="lab-grown">
    <div
        data-aos="zoom-in"
        data-aos-offset="300px"
        data-aos-delay="300"
        data-aos-duration="400"
        data-aos-easing="linear"
        class="lab-grown__title">
      <Typography :heading="2">
        Lab Grown
      </Typography>
    </div>
    <div class="lab-grown__1">
      <v-lazy-image class="block w-100 mb-2" alt="Lab Grown - Live Diamond" width="460" height="467"
           data-aos="zoom-out-up"
           data-aos-offset="300px"
           data-aos-delay="400"
           data-aos-duration="400"
           data-aos-easing="linear"
           src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/best_seller_wPlcMH35g.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658745030726" />
      <div data-aos="zoom-in"
           data-aos-offset="300px"
           data-aos-delay="300"
           data-aos-duration="400"
           data-aos-easing="linear">
        <Text>
          Dalle linee più classiche fino ad arrivare a modelli più moderni che conservano l’eleganza del Made In Italy,
          tutti i diamanti Live Diamond possiedono le stesse caratteristiche di lucentezza, purezza e caratura di un
          diamante tradizionale.
        </Text>
      </div>

    </div>
    <div class="lab-grown__2">
      <v-lazy-image class="block w-100 mb-2" alt="Lab Grown - Live Diamond" width="403" height="627"
           data-aos="zoom-out-up"
           data-aos-offset="300px"
           data-aos-delay="800"
           data-aos-duration="400"
           data-aos-easing="linear"
           src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/placeholder_VJRL9WOmp.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658745487441" />
      <div class="lab-grown-carousel mb-2">
        <CarouselVue :slide="slides"></CarouselVue>
      </div>
      <div class="text-center"
           data-aos="zoom-in"
           data-aos-offset="300px"
           data-aos-delay="300"
           data-aos-duration="400"
           data-aos-easing="linear"
      >
        <Link :link="linkButton">
          acquista i best seller
        </Link>
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

const linkButton = 'https://www.bluespirit.com/live-diamond-live-diamond-B222N5634.htm';

const slides = [
  {
    title: 'Live Diamond - Best Seller 1',
    link: 'https://www.bluespirit.com/collana-live-diamond-live-diamond-ld00508-P73403.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bestseller_1_Rq7MNmoRp.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412518'
  },
  {
    title: 'Live Diamond - Best Seller 2',
    link: 'https://www.bluespirit.com/collana-live-diamond-lab-grown-p77q310000600-P68708.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bestseller_2_Wc7apzvAy.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755414390'
  },
  {
    title: 'Live Diamond - Best Seller 3',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld04034010i-P79755.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bestseller_3_OBzeSLMRB.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412531'
  },
  {
    title: 'Live Diamond - Best Seller 4',
    link: 'https://www.bluespirit.com/orecchini-live-diamond-live-diamond-ld01002-P73406.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/bestseller_4_MBwKRfCQDS.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658755412518'
  }
];

onMounted(() => {
  AOS.init();
});
</script>

<style scoped lang="scss">
.lab-grown {
  padding-left: 10%;
  padding-right: 10%;
  display: flex;
  align-items: flex-start;
  margin-bottom: 5rem;
  position: relative;
}

.lab-grown__1 {
  flex: 0 0 40%;
  max-width: 40%;
  padding: 0 15px;
}

.lab-grown__2 {
  flex: 0 0 35%;
  max-width: 35%;
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

.lab-grown__title {
  position: absolute;
  width: 30%;
  right: 0;
  z-index: 2;
}

.lab-grown-carousel {
  width: 100%;
  max-width: 380px;
  display: block;
  margin: 0 auto;
  margin-bottom: 2rem;
  border: 2px solid #215732;
}

.text-center {
  text-align: center;
}

@media (max-width: 1100px) {
  .lab-grown {
    padding-left: 15px;
    padding-right: 15px;
  }
}

@media (max-width: 991px) {
  .lab-grown {
    padding-top: 116px;
  }

  .lab-grown__1 {
    flex: 0 1 50%;
    max-width: 50%;
    padding: 0 15px;
  }

  .lab-grown__2 {
    flex: 0 1 50%;
    max-width: 50%;
    padding: 0 15px;
  }
  .lab-grown__title {
    width: 100%;
    top: 0;
    text-align: center;
  }
}

@media (max-width: 767px) {
  .lab-grown {
    flex-wrap: wrap;
  }
  .lab-grown__1 {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0px;
  }

  .lab-grown__2 {
    flex: 0 0 100%;
    max-width: 100%;
    padding: 0px;
  }
}
</style>