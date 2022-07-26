<template>
  <div class="hero">
    <img alt="" src="../assets/logo.svg" class="hero__logo"/>
    <div class="hero__content">
      <div class="relative hero-image-title">
        <img
            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Hero_6ZiSMKKI7.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1658740032560"
            data-aos="zoom-out-up"
            data-aos-offset="300px"
            data-aos-delay="300"
            data-aos-duration="400"
            data-aos-easing="linear"
        >
        <div class="hero-image-title__title">
          <Typography :heading="1">
            Il Diamante che ama il pianeta
          </Typography>
        </div>
      </div>
      <div class="text-center"
           data-aos="zoom-in"
           data-aos-offset="300px"
           data-aos-delay="300"
           data-aos-duration="400"
           data-aos-easing="linear"
      >
        <Text>
          Live Diamond è il brand italiano di diamanti accresciuti in laboratorio, ecologici e socialmente compatibili.
        </Text>
        <Text>
          Ogni diamante viene realizzato in laboratorio, attraverso un processo all’avanguardia che dà vita a pietre di
          grande qualità ma senza estrarle dal suolo, limitando i danni per l’ambiente.
        </Text>
        <Link :link="linkButton">
          Scopri Live Diamond
        </Link>
      </div>
    </div>
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
  padding-left: 7%;
  padding-right: 14%;
  display: flex;
  align-items: flex-start;
  margin-bottom: 5rem;
}

.hero__logo {
  flex: 0 0 150px;
  max-width: 150px;
}

.hero__content {
  flex: 1 0 calc(100% - 150px);
  max-width: calc(100% - 150px);
  padding: 0 15px;
}

.relative {
  position: relative;
}

.hero-image-title {
  display: flex;
  justify-content: center;
  width: 100%;
  margin-bottom: 3rem;

  img {
    flex: 1 0 80%;
    max-width: 80%;
  }
}

.hero-image-title__title {
  text-align: center;
  transform: rotate(-90deg) translate(-70%, 100%);
  position: absolute;
  top: 0%;
  max-width: 350px;
  right: 0;
}

.text-center {
  text-align: center;
}

@media (max-width: 1400px){
  .hero-image-title__title {
    transform: rotate(-90deg) translate(-50%, 110%);
  }
}

@media (max-width: 1300px){
  .hero-image-title {
    flex-direction: column;
    img{
      max-width: 100%;
      flex: 0 0 auto;
    }
  }
  .hero-image-title__title{
    transform: none;
    position: relative;
    display: block;
    margin: 0 auto;
  }

  .hero__content {
    flex: 1 0 calc(100%);
    max-width: calc(100%);
    padding: 0 15px;
  }
}

@media (max-width: 991px){
  .hero {
    padding-left: 15px;
    padding-right: 15px;
    flex-direction: column;
    align-items: center;
  }
  .hero__content {
    padding: 0px;
  }
}

</style>