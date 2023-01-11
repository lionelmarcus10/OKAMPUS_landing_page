<template>
  <swiper
    :slidesPerView="1"
    :spaceBetween="30"
    :loop="true"
    :speed="1500"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :modules="modules"
    class="mySwiper"

  >
    <swiper-slide>
      <div class="w-9/12 md:w-7/12 xl:w-4/12 mx-auto">
      <img src="../assets/typo.png" alt="" srcset="" class="border border-2 border-solid border-blue-500">
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="w-9/12 md:w-7/12 mx-auto xl:w-4/12">
        <img src="../assets/typo.png" alt="" srcset="" class="border border-2 border-solid border-blue-500">
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="w-9/12 md:w-7/12 mx-auto xl:w-4/12">
        <img src="../assets/typo.png" alt="" srcset="" class="border border-2 border-solid border-blue-500">
      </div>
    </swiper-slide>
  </swiper>

</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination, Navigation, Autoplay } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation, Autoplay],
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
  background: transparent;

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
  margin-left: auto;
  margin-right: auto;
}

</style>
