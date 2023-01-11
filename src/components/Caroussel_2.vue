<template>
<div class="">
    <swiper
    :modules="modules"
    :loop="true"
    :speed="1500"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :centeredSlides="true"
    :spaceBetween="30"
    :pagination="{
      clickable: true,
    }"
    :virtual="true"
    class="mySwiper"
    @swiper="setSwiperRef"
    >
    <swiper-slide
        class="bg-red-500"
        v-for="(slideContent, index) in slides"
        :key="index"
        :virtualIndex="index"
        >{{ slideContent }}</swiper-slide
    >
    </swiper>
</div>
</template>
<script>
import { ref } from 'vue';
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';
import 'swiper/css/virtual';

// import Swiper core and required modules
import { Pagination, Navigation, Virtual, Autoplay } from 'swiper';

export default {
    components: {
    Swiper,
    SwiperSlide,
    },
    setup() {
    // Create array with 500 slides
    const slides = ref(
        Array.from({ length: 6 }).map((_, index) => `Slide ${index + 1}`)
    );
    let swiperRef = null;
    let appendNumber = 6;
    let prependNumber = 1;

    const setSwiperRef = (swiper) => {
        swiperRef = swiper;
    };
    const slideTo = (index) => {
        swiperRef.slideTo(index - 1, 0);
    };
    const append = () => {
        slides.value = [...slides.value, 'Slide ' + ++appendNumber];
    };
    const prepend = () => {
        slides.value = [
        `Slide ${prependNumber - 2}`,
        `Slide ${prependNumber - 1}`,
        ...slides.value,
        ];
        prependNumber -= 2;
        swiperRef.slideTo(swiperRef.activeIndex + 2, 0);
    };
    return {
        slides,
        swiperRef: null,
        appendNumber,
        prependNumber,
        setSwiperRef,
        slideTo,
        append,
        prepend,
        modules: [Pagination, Navigation, Virtual,Autoplay],
    };
    },
};
</script>
<style scoped>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.swiper {
  width: 100%;
  height: 300px;
  margin: 20px auto;
}
.append-buttons {
  text-align: center;
  margin-top: 20px;
}

.append-buttons button {
  display: inline-block;
  cursor: pointer;
  border: 1px solid #007aff;
  color: #007aff;
  text-decoration: none;
  padding: 4px 10px;
  border-radius: 4px;
  margin: 0 10px;
  font-size: 13px;
}

</style>