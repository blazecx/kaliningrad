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
      <div class="contentiner">
        <div class="content" id="img21">
          <h5>Кафедральный собор</h5>
        </div>
        <div class="content" id="img22">
          <h5>Крепость Врангеля</h5>
        </div>
        <div class="content" id="img23">
          <h5>Форт №5</h5>
        </div>
        <div class="content" id="img24">
          <h5>Рыбацкая деревня</h5>
        </div>
      </div>
    </section>
    <section class="section-five">
      <h1>Лента времени</h1>
      <swiper  @slideChange="2" :slidesPerView="4" :spaceBetween="30" :centeredSlides="true" :loop="true" :pagination="{
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
  font-size: 3rem;
  color: #791100;
  font-weight: 500;
}

p {
  font-family: "DM Sans", sans-serif;
  font-size: 1rem;
}

.section-two,
.section-three,
.section-four,
.section-six,
.section-five {
  margin-top: 6.25rem;
  margin-left: 19.375rem;
  margin-right: 19.375rem;
}

.section-one {
  background: url("./components/icons/mainPage.png");
  background-repeat: no-repeat;
  height: 100vh;
}


.section-two .container h2 {
  margin-left: 48rem;
}

.section-two .museum {
  position: relative;
  margin-left: 35rem;
  margin-top: 11.875rem;
}

.section-two .sobor {
  position: absolute;
  margin-left: 53.125rem;
  margin-top: 3.125rem;
}

.section-two .container-two p {
  position: absolute;
  margin-top: 7.5rem;
}

.section-two .minimap {
  margin-left: 3.125rem;
}

.section-two .conteiner-three {
  margin-left: 3.75rem;
}

.section-two .conteiner-three p {
  margin-left: 24.375rem;
}

.section-two .conteiner-four {
  margin-top: 2.75rem;
  display: flex;
}

.section-two .conteiner-four .conrainer-five {
  margin-top: 8.125rem;
}

.section-two .conteiner-four .conrainer-five p {
  margin-top: 1.25rem;
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
  padding-top: .5rem;
}

.section-three .container .content:nth-child(3) {
  padding-top: .5rem;
}

#img1,
#img2,
#img3,
#img4 {
  width: 19.375rem;
  height: 14.6875rem;

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
  gap: .5rem;

}

.section-three .container {
  margin-top: 3.125rem;
  gap: 0.5rem;
}

.section-four .contentiner{
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.section-four .contentiner .content{
  display: flex;
  justify-content: center;
}

h5{
  margin-top: 1.875rem;
  font-family: "Fira Code";
  font-size: 1.125rem;
  font-weight: bold;
  color: white;
}

#img21, #img22, #img23, #img23, #img24{
  width: 19.375rem;
  height: 28.25rem;
}

#img21{
background: url(./components/icons/kafsobor.png);
}

#img22{
  background: url(./components/icons/vrangel.png);
}

#img23{
  background: url(./components/icons/fort5.png);
}

#img24{
  background: url(./components/icons/vilage.png);
}

/* swiper */
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

.swiper-slide .content {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 26.25rem;
  height: 11.875rem;
  background: #FC8A4C;
  border-radius: 15px;
}

.section-six {
  width: 75rem;
  height: 29.875rem;
  border-radius: 2.1875rem;
  background: linear-gradient(to right, #FD6A21, #FB9E40);
  padding-top: 2.5rem;
  padding-left: 6.875rem;
  color: white;
}

.section-six h4 {
  font-family: "Fira Code";
  font-size: 2rem;
  font-weight: bold;
}

.section-six .con p:first-child {
  margin-top: 1.125rem;
  font-family: "DM Sans", sans-serif;
  font-size: 1rem;
}

.section-six .con p:last-child {
  margin-top: 1.75rem;
  font-family: "DM Sans", sans-serif;
  font-size: 1rem;
  color: black;
}

.section-six .labeltext {
  margin-top: 1.125rem;
  width: 30.125rem;
  height: 2.75rem;
  border: none;
  border-radius: 1.5625rem;
}

.section-six .contei {
  margin-top: 1.625rem;
  margin-right: 39.375rem;
  padding-right: 9.375rem;
  display: flex;
  color: black;
}

.section-six .contei p {
  margin-top: .125rem;
}

.section-six .contei .checkbox {
  cursor: pointer;
  border: 1px solid black;
  width: 1.25rem;
  height: 1.25rem;
  background: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

.section-six .contei .checkbox:checked::before {
  content: '\2713'; /* Юникод символ галочки */
  color: #791100; /* Цвет галочки */
  font-size: 1.25rem; /* Размер шрифта */
  position: relative; /* Позиционирование */
  top: -0.375rem; /* Выравнивание по вертикали */
  left: .125rem; /* Выравнивание по горизонтали */

}


button {
  margin-top: 2.375rem;
  width: 15.25rem;
  height: 3rem;
  border-radius: 1.25rem;
  border: none;
  background: black;
  color: white;
  font-size: 1.375rem;
  cursor: pointer;
}
</style>
