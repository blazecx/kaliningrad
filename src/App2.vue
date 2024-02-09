<template>
  <swiper @slideChange="2" :slidesPerView="4" :spaceBetween="30" :centeredSlides="true" :pagination="{
    clickable: true,
  }" :modules="modules" class="mySwiper">
    <swiper-slide><img src="https://w.forfun.com/fetch/da/daf8eb568fea522f6701fb9c66378cdc.jpeg" alt=""></swiper-slide>
    <swiper-slide><img
        src="https://mykaleidoscope.ru/x/uploads/posts/2022-10/1666206241_12-mykaleidoscope-ru-p-kartinka-na-zastavku-oboi-12.jpg"
        alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
    <swiper-slide> <img src="" alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
    <swiper-slide><img src="" alt=""></swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';


// import required modules
import { Pagination, FreeMode } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [FreeMode],
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
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>