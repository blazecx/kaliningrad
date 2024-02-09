<template>
  <div class="swiper-container" ref="swiperContainer">
    <swiper class="swiper-wrapper">
      <div
        v-for="(slide, index) in slides"
        :key="index"
        class="swiper-slide"
        :style="{ backgroundColor: slide.color }"
        @mouseover="showImage(index)"
        @mouseleave="hideImage(index)"
        @click="showModal(index)"
      >
        <swiper-slide v-if="slide.image" class="slide-image" :style="{ backgroundImage: `url(${slide.image})` }"></swiper-slide>
        <div v-else class="slide-text">{{ slide.date }}</div>
      </div>
    </div>
  </swiper>
  <div v-if="modalVisible" class="modal" @click="hideModal">
    <div class="modal-content">
      <p>{{ modalContent }}</p>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

import 'swiper/css/navigation';



import './style.css'

// import required modules
import { Pagination, FreeMode } from 'swiper/modules';


export default {
  data() {
    return {
      swiper: null,
      modalVisible: false,
      modalContent: '',
      slides: [
        { color: 'orange', date: '1 января', image: null },
        // ... остальные слайды
      ],
    };
  },
  mounted() {
    this.swiper = new Swiper(this.$refs.swiperContainer, {
      // Настройки Swiper
    });
  },
  methods: {
    showImage(index) {
      // Отображение картинки при наведении
      this.slides[index].image = 'path/to/image.jpg'; // Замените на путь к нужной картинке
    },
    hideImage(index) {
      // Скрытие картинки при уходе курсора
      this.slides[index].image = null;
    },
    showModal(index) {
      this.modalContent = this.slides[index].date;
      this.modalVisible = true;
    },
    hideModal() {
      this.modalVisible = false;
    },
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<style>
.swiper-container {
  width: 100%;
  height: 400px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide-image {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
}

.slide-text {
  padding: 50px;
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background: #fff;
  padding: 20px;
  border-radius: 5px;
}
</style>