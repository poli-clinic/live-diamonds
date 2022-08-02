<template>
  <carousel :items-to-show="1" :autoplay="2000" :wrap-around="true">
    <slide v-for="slide in slides" :key="slide">
      <div class="carousel__item">
        <a :href="slide.link">
          <img ref="bg-slide" :alt="slide.title" :title="slide.title" :src="slide.image" width="530" height="530">
        </a>
      </div>
    </slide>
    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import {ref} from 'vue';
/*! purgecss start ignore */
import 'vue3-carousel/dist/carousel.css';
/*! purgecss end ignore */
import {Carousel, Slide, Navigation} from 'vue3-carousel';


export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Navigation
  },
  props: {
    slide: {
      type : Array,
      required: true,
    }
  },
  setup(props) {
    // make users variable reactive with the ref() function
    console.log(props);
    const slides = ref(props.slide);
    return {
      slides
    };
  }
};
</script>

<style lang="scss">
/* purgecss start ignore */

.carousel__item {
  height: 0;
  padding-bottom: 100%;
  width: 100%;
  color: var(--vc-clr-white);
  font-size: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  //border: 2px solid #215732;
  img {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
    top: 0;
    left: 0;
    transition: all .2s ease-in-out;
  }
  &:hover{
    img{
      transform: scale(1.1);
    }
  }
}

.carousel__icon {
  fill: #1A5632;
  width: 50px;
  height: 50px;
}

.carousel__next {
  transform: translate(0%, -50%);
}

.carousel__prev {
  transform: translate(0%, -50%);
}

.carousel__prev, .carousel__next {
  background-color: transparent;
  border-radius: 0;
  width: 50px;
  height: 50px;
}

@media (max-width: 768px){
  .carousel__prev, .carousel__next {
    display: none;
  }
}

/* purgecss end ignore */
</style>