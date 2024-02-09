<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

import 'swiper/css/navigation';

import './style.css';
// import required modules
import { Pagination, FreeMode } from 'swiper/modules';


export default {
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

<template>
  <div>
    <section class="section-one">
      <p>Горд - где море встречается с историей!</p>
      <nav>
        <a>История</a>
        <a>Новости</a>
        <a>Контакты</a>
      </nav>
    </section>
    <section class="section-two">
      <div class="container">
        <h1>Город, где встречается История</h1>
        <h2>и современность</h2>
      </div>
      <div class="container-two">
        <p>За последние 500 лет город Клининград, известный так же как <br>
          Кёнинсберг, прошёл через ряд значимых исторических событий. <br>
          Город был частью Тевтонского ордена, Пруссии, Германии и СССР <br>
          Город имеет богатое наследие немецкой и советской архетектуры</p>
        <div class="page">
          <img src="./components/icons/sobor_one.png" alt="" class="sobor">
          <img src="./components/icons/museum_one.png" alt="" class="museum">
        </div>
      </div>
      <div class="conteiner-three">
        <img src="./components/icons/minimap.png" alt="" class="miniMap">
        <p>Сегодня Калининград является самым западным регионом <br>
          России. Также это единственный регион, полностью <br>
          окружён территорией другой страны - Польшей и Литвой</p>
      </div>
      <div class="conteiner-four">
        <div class="conrainer-five">
          <img src="./components/icons/beach-one.png" alt="">
          <p>Калининград находиться на берегу балтийского моря. <br>
            Мягкие песчаные пляжи, бодрящая вода и свежий <br>
            морской бриз создают идеальные условия для отдыха и туризма</p>
        </div>
        <img src="./components/icons/bigMap.svg" alt="">
      </div>
    </section>
    <section class="section-three">
      <h1>Интересные факты</h1>
      <div class="container">
        <div class="content" id="img1">
          <p>Население</p>
          <p>489 735 чел. <br></p>
        </div>
        <div class="content" id="img2">
          <p>Пляжи</p>
          <p>Все пляжи бесплатные <br></p>
        </div>
        <div class="content" id="img3">
          <p>Вода</p>
          <p>Воду можно пить <br>
            из под крана</p>
        </div>
        <div class="content" id="img4">
          <p>Клопсы</p>
          <p>Одно из <br>
            популярных блюд</p>
        </div>
      </div>
    </section>
    <section class="section-four">
      <h1>Главные достопримечательности</h1>
    </section>
    <section class="section-five">
      <h1>Лента времени</h1>
      <swiper @slideChange="2" :slidesPerView="4" :spaceBetween="30" :centeredSlides="true" :pagination="{
        clickable: true,
      }" :modules="modules" class="mySwiper">
        <swiper-slide>
          <div class="content">
            <h3>1947</h3>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="content">
            <h3>1255</h3>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="content">
            <h3>1701</h3>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="content">
            <h3>1945</h3>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="content">
            <h3>1946</h3>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="content">
            <h3>1991</h3>
          </div>
        </swiper-slide>
      </swiper>
    </section>
  </div>
  <section class="section-six">
    <h4>Будь в курсе</h4>
    <div class="con">
      <p>Подпишись на нашу рассылку о новых <br>
        мероприятиях и местах в Калининграде</p>
      <p>E-mail</p>
    </div>
    <input type="text" class="labeltext">
    <div class="contei">
      <input type="checkbox" name="" id="" class="checkbox">
      <p>Соглашаюсь с Правилами рассылок</p>
    </div>
    <button>ПОДПИСАТЬСЯ</button>
  </section>
</template>

<style scoped>
* {
  margin: 0 auto;
  padding: 0;
  box-sizing: border-box;
}

@font-face {
  font-family: "Fira Code";
  src: url("src/assets/Fira_Code/static/FiraCode-Bold.ttf");
}

@font-face {
  font-family: "Fira Code";
  src: url("src/assets/Fira_Code/static/FiraCode-Light.ttf");
}

@font-face {
  font-family: "Fira Code";
  src: url("src/assets/Fira_Code/static/FiraCode-Medium.ttf");
}

@font-face {
  font-family: "Fira Code";
  src: url("src/assets/Fira_Code/static/FiraCode-Regular.ttf");
}

@font-face {
  font-family: "Fira Code";
  src: url("src/assets/Fira_Code/static/FiraCode-SemiBold.ttf");
}

@font-face {
  src: url("@/src/assets/DM_Sans/static/DMSans-Regular.ttf");
  font-family: "DM Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

h1,
h2 {
  font-family: "Fira Code";
  font-size: 48px;
  color: #791100;
  font-weight: 500;
}

p {
  font-family: "DM Sans", sans-serif;
  font-size: 16px;
}

.section-two,
.section-three,
.section-four,
.section-six,
.section-five {
  margin-top: 100px;
  margin-left: 310px;
  margin-right: 310px;
}

.section-one {
  background: url("./components/icons/mainPage.png");
  background-repeat: no-repeat;
  height: 100vh;
}


.section-two .container h2 {
  margin-left: 768px;
}

.section-two .museum {
  position: relative;
  margin-left: 560px;
  margin-top: 190px;
}

.section-two .sobor {
  position: absolute;
  margin-left: 850px;
  margin-top: 50px;
}

.section-two .container-two p {
  position: absolute;
  margin-top: 120px;
}

.section-two .minimap {
  margin-left: 50px;
}

.section-two .conteiner-three {
  margin-left: 60px;
}

.section-two .conteiner-three p {
  margin-left: 390px;
}

.section-two .conteiner-four {
  margin-top: 44px;
  display: flex;
}

.section-two .conteiner-four .conrainer-five {
  margin-top: 130px;
}

.section-two .conteiner-four .conrainer-five p {
  margin-top: 20px;
}

.section-three .container {
  display: flex;
  flex-wrap: wrap;
}

.section-three .container p:first-child {
  font-family: "Fira Code";
  color: white;
  font-weight: bolder;
}

.section-three .container p:last-child {
  font-family: "DM Sans";
  color: white;
  font-weight: normal;
  text-align: center;
}

.section-three .container .content:nth-child(4) {
  padding-top: 8px;
}

.section-three .container .content:nth-child(3) {
  padding-top: 8px;
}

#img1,
#img2,
#img3,
#img4 {
  width: 310px;
  height: 235px;

}

#img1 {
  background: url(./components/icons/civil.png);
}

#img2 {
  background: url(./components/icons/beach.png);
}

#img3 {
  background: url(./components/icons/wother.png);
}

#img4 {
  background: url(./components/icons/clopce.png);
}

.section-three .container .content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 8px;

}

.section-three .container {
  margin-top: 50px;

}

/* swiper */
.swiper {
  margin-top: 50px;
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

.swiper-slide .content {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 420px;
  height: 190px;
  background: #FC8A4C;
  border-radius: 15px;
}

.section-six {
  width: 1200px;
  height: 478px;
  border-radius: 35px;
  background: linear-gradient(to right, #FD6A21, #FB9E40);
  padding-top: 40px;
  padding-left: 110px;
  color: white;
}

.section-six h4 {
  font-family: "Fira Code";
  font-size: 32px;
  font-weight: bold;
}

.section-six .con p:first-child {
  margin-top: 18px;
  font-family: "DM Sans", sans-serif;
  font-size: 16px;
}

.section-six .con p:last-child {
  margin-top: 28px;
  font-family: "DM Sans", sans-serif;
  font-size: 16px;
  color: black;
}

.section-six .labeltext {
  margin-top: 18px;
  width: 482px;
  height: 44px;
  border: none;
  border-radius: 25px;
}

.section-six .contei {
  margin-top: 26px;
  margin-right: 630px;
  padding-right: 150px;
  display: flex;
  color: black;
}

.section-six .contei p {
  margin-top: 2px;
}

.section-six .contei .checkbox {
  cursor: pointer;
  border: 1px solid black;
  width: 20px;
  height: 20px;
  background: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

.section-six .contei .checkbox:checked {}


button {
  margin-top: 38px;
  width: 244px;
  height: 48px;
  border-radius: 20px;
  border: none;
  background: black;
  color: white;
  font-size: 22px;
  cursor: pointer;
}
</style>
