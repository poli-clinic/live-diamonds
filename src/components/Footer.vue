<template>
  <div class="block text-center footer-title" data-sal="slide-down">
    <div class="block text-center">
      <Typography :heading="2">In tendenza?</Typography>
    </div>
    <div class="block text-center">
      <Typography :heading="1">Il multi-indosso</Typography>
    </div>
  </div>
  <div class="block text-center footer-text" data-aos="fade-down">
    <Text>
      <strong>L’oro</strong> e <strong>i diamanti</strong> si uniscono per farti risplendere nei tuoi momenti speciali: sono perfetti per
      essere mixati tra loro e creare degli abbinamenti eleganti e mai banali.
    </Text>
  </div>
  <div class="footer iframe" style="background-image: url('https://ik.imagekit.io/vj78ie3kf/Live_Diamond/LD_9_3mb_edit_2_8n-o79g2Y.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1663688287346'); background-size: cover; background-repeat: no-repeat"
       data-video="https://player.vimeo.com/video/751165464?h=2e3b797906&badge=0&autoplay=1&muted=1&background=1&autopause=0&player_id=0&app_id=58479">
  </div>
  <div class="text-center footer__link">
    <Link :link="linkButton">Lasciati ispirare</Link>
  </div>
</template>

<script setup>
import {onMounted} from "@vue/runtime-core";
import Typography from "./Typography.vue";
import Text from "./Text.vue";
import Link from "./Link.vue";
import AOS from "aos";
import 'aos/dist/aos.css'

const linkButton = 'https://www.bluespirit.com/live-diamond-B222.htm';

onMounted(() => {
  AOS.init({
    mirror:false,
    once: true
  });

  const sections = document.querySelectorAll('[data-video]')
  const options = {
    threshold: 0
  }
  const observer = new IntersectionObserver(function(entries, observer) {
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

function createIframe(url){
  return '<iframe src="' + url + '" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%; z-index: 9;" title="Video - Live Diamond" alt="Video - Live Diamond"></iframe>';
}
</script>

<style scoped>
.iframe{
  opacity: 1;
  visibility: visible;
  transition: all 2s linear;
}

.iframe-hidden{
  opacity: 0;
  visibility: hidden;
}

.footer-title {
  margin-bottom: 40px;
}

.footer {
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

.block {
  display: block;
}

.text-center {
  text-align: center;
}

.footer-text {
  max-width: 1088px;
  width: 100%;
  margin: 0 auto 40px;
}

.footer__link{
  margin-bottom: 100px;
}

@media (max-width: 768px){
  .footer__link{
    margin-bottom: 70px;
  }
}

</style>