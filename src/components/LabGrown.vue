<template>
  <div class="block text-center lab-grown-title" data-aos="fade-down">
    <Typography :heading="2">Una scelta</Typography>
    <Typography :heading="1">&nbsp;d'amore</Typography>
  </div>
  <div class="lab-grown iframe" style="background-image: url('https://ik.imagekit.io/vj78ie3kf/Live_Diamond/LD_1_6mb_edit_1__9za6nWu8v.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1663688213430'); background-size: cover; background-repeat: no-repeat"
       data-video="https://player.vimeo.com/video/751165343?h=4dd3b5c4ec&badge=0&autoplay=1&muted=1&background=1&autopause=0&player_id=0&app_id=58479">
  </div>
  <div class="lab-grown-content__text-mobile text-center show-mobile" data-aos="fade-down">
    <Text>
      Eleganza e design <strong>Made In Italy</strong> caratterizzano tutti i diamanti Live Diamond, che possiedono le stesse
      caratteristiche di lucentezza, purezza e caratura di un diamante tradizionale.<br>
      Inoltre <strong>l'oro</strong> utilizzato da Live
      Diamond è oro <strong>riciclato</strong> proveniente da fonti certificate, una scelta all'insegna del rispetto della natura.
    </Text>
  </div>
  <div class="lab-grown-content">
    <div class="lab-grown-content__images">
      <picture class="lab-grown-content__image" data-aos="zoom-out-up" data-aos-easing="linear" data-aos-duration="500">
        <source
            media="(max-width: 768px)" width="445" height="691"
            srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/verticale_2_375l1-Bes.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439298">
        <v-lazy-image
            class="img-cover" alt="Una scelta d'amore - Live Diamond" width="950" height="1170"

            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Verticale_2_gdmU3Y--v.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659346866471"/>
      </picture>
      <picture class="lab-grown-content__image" data-aos="zoom-out-up" data-aos-easing="linear" data-aos-duration="500">
        <source
            media="(max-width: 768px)" width="445" height="691"
            srcset="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/mobile/verticale_1_UTCgjdmPW.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659357439308">
        <v-lazy-image
            class="img-cover" alt="Una scelta d'amore - Live Diamond" width="950" height="1170"
            src="https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Vericale_1_kDvM6p9S2.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659346866613"/>
      </picture>
    </div>
    <div class="lab-grown-content__text hidden-mobile" data-aos="fade-down">
      <Text>
        Eleganza e design <strong>Made In Italy</strong> caratterizzano tutti i diamanti Live Diamond, che possiedono le stesse
        caratteristiche di lucentezza, purezza e caratura di un diamante tradizionale.<br>
        Inoltre <strong>l'oro</strong> utilizzato da Live
        Diamond è oro <strong>riciclato</strong> proveniente da fonti certificate, una scelta all'insegna del rispetto della natura.
      </Text>
    </div>
  </div>
  <div class="prodotti-container">
    <div class="prodotti">
      <div class="prodotto" v-for="s in slides" :key="s">
        <a :href="s.link">
          <div class="prodotto__img">
            <img :src="s.image" :alt="s.title" :title="s.title" class="img-cover" data-aos="fade-up"
                 data-aos-duration="1000" data-aos-offset="300">
          </div>
        </a>
      </div>
    </div>
  </div>
  <div class="text-center lab-grown__link" data-aos="fade-down">
    <Link :link="linkButton">Acquista i best seller</Link>
  </div>
</template>

<script setup>
import {onMounted} from "@vue/runtime-core";
import Observer from 'intersection-observer';
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
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD00508_best_seller_jpg_QPPaHFYhe.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729206'
  },
  {
    title: 'Live Diamond - Best Seller 2',
    link: 'https://www.bluespirit.com/collana-live-diamond-lab-grown-p77q310000600-P68708.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/P.77Q310000600_best_seller_pnBtwy22Ws.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365730070'
  },
  {
    title: 'Live Diamond - Best Seller 3',
    link: 'https://www.bluespirit.com/anello-live-diamond-live-diamond-ld04034010i-P79755.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD04034010I_best_seller_5C3qsaip5.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365730176'
  },
  {
    title: 'Live Diamond - Best Seller 4',
    link: 'https://www.bluespirit.com/orecchini-live-diamond-live-diamond-ld01002-P73406.htm',
    image: 'https://ik.imagekit.io/vj78ie3kf/Live_Diamond/Caroselli/LD01002_best_sellerjpg_v7PFNIRzK.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1659365729666'
  }
];

onMounted(() => {

  AOS.init({
    mirror: false,
    once: true
  });

  const sections = document.querySelectorAll('[data-video]')
  const options = {
    threshold: 0
  }
  const observer = new IntersectionObserver(function (entries, observer) {
    entries.forEach(entry => {
      if (entry.isIntersecting && !entry.target.classList.contains('stop')) {
        entry.target.classList.add('stop');
        let url = entry.target.getAttribute('data-video');
        entry.target.innerHTML = createIframe(url);
        entry.target.classList.remove('iframe-hidden');
        entry.target.removeAttribute('data-video');
      }
    })
  }, options)
  sections.forEach(section => {
    observer.observe(section)
  })
});

function createIframe(url) {
  return '<iframe src="' + url + '" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%; z-index: 9;" title="Video - Live Diamond" alt="Video - Live Diamond"></iframe>';
}

</script>

<style scoped lang="scss">
.iframe {
  opacity: 1;
  visibility: visible;
  transition: all 2s linear;
}

.iframe-hidden {
  opacity: 0;
  visibility: hidden;
}

.lab-grown-title {
  margin-bottom: 40px;
}

.lab-grown {
  height: 0;
  padding-bottom: 56.25%;
  width: 100%;
  position: relative;
  margin-bottom: 40px;
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

.lab-grown-content {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 105%;
  margin-bottom: 40px;
}

.lab-grown-content__images {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.lab-grown-content__image {
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

.lab-grown-content__text {
  width: 42%;
  height: 28%;
  position: absolute;
  text-align: center;
  bottom: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;

  p {
    padding: 15px 70px;
    margin-bottom: 0;
  }
}

.prodotti {
  display: flex;
  margin-left: -8px;
  margin-right: -8px;
  flex-wrap: wrap;
  margin-bottom: 40px;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
}

.prodotto {
  flex: 0 0 25%;
  max-width: 25%;
  padding-left: 8px;
  padding-right: 8px;
}

.prodotto__img {
  width: 100%;
  position: relative;
  border: 2px solid #1A5632;
  padding-bottom: 100%;
  box-sizing: border-box;
  overflow: hidden;

  img {
    transition: all .2s ease-in-out !important;
  }

  &:hover {
    img {
      transform: scale(1.1) !important;
    }
  }
}

.lab-grown__link {
  margin-bottom: 100px;
}

@media (max-width: 1100px) {
  .lab-grown-content__text {
    p {
      padding: 15px 15px;
    }
  }
}

.show-mobile {
  display: none;
}

@media (max-width: 768px) {
  .hidden-mobile {
    display: none;
  }
  .show-mobile {
    display: block;
  }
  .lab-grown__link {
    margin-bottom: 70px;
  }
  .lab-grown-content {
    padding-bottom: 115%;
  }
  .lab-grown-content__image {
    padding-bottom: 73%;
  }
  .prodotti {
    width: 175%;
    padding-left: 22px;
  }
  .prodotti-container {
    width: 100%;
    overflow-x: auto;
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
  .prodotti-container::-webkit-scrollbar {
    display: none;
  }
}

</style>