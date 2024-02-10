<script>
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
      modalVisible: false,
      modalText: '',
      slides: [
        { text: 'src/components/SwiperIMG/Group 21.png', modalText: '1255 год в Калининграде (тогда это был Кёнигсберг) был годом, когда город был основан Тевтонским орденом. Кёнигсберг был основан на месте древнепрусского поселения, и его название означает "королевский холм" на немецком языке. Город стал важным политическим, экономическим и культурным центром в регионе и был столицей Восточной Пруссии до Второй мировой войны. В 1946 году после войны город был переименован в Калининград в честь советского политического деятеля Михаила Калинина, и он стал частью Советского Союза.' },
        { text: 'src/components/SwiperIMG/Group 22.png', modalText: 'Это модальное окно 2' },
        { text: 'src/components/SwiperIMG/Group 23.png', modalText: 'Это модальное окно 3' },
        { text: 'src/components/SwiperIMG/Group 20.png', modalText: 'Это модальное окно 3' },
        { text: 'src/components/SwiperIMG/Group 19.png', modalText: 'Это модальное окно 3' },
      ],
    };
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
  methods: {
    openModal(index) {
      this.modalVisible = true;
      this.modalText = this.slides[index].modalText;
    },
    closeModal() {
      this.modalVisible = false;
    },
  },
  mounted() {
    const swiper = new Swiper('.swiper-container', {
      // ...
    });
  },
};
</script>

<template>

    <swiper  @slideChange="2" :slidesPerView="4" :spaceBetween="30" :centeredSlides="true"  :pagination="{
        clickable: true,
      }" :modules="modules" class="mySwiper">
  
        <swiper-slide v-for="(slide, index) in slides" :key="index" @click="openModal(index)">
          <img :src="slide.text" alt="">
        </swiper-slide>

    </swiper>

    <div v-if="modalVisible" class="modal">
      <div class="modal-content">
        <p class="modal-text">{{ modalText }}</p>
        <button @click="closeModal">Закрыть</button>
      </div>
    </div>

</template>



<style scoped>
.swiper {
  margin-top: 3.125rem;
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 1.125rem;
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


.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
  text-align: center;
}

.modal-text{
width: 20rem;
}

</style>