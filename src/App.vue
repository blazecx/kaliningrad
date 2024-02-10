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
      hover: null,
      contents: [
        { id: 'img21', imageUrl: 'src/components/icons/kafsobor.png', title: 'Кафедральный собор в Калининграде - это одна из главных достопримечательностей города.Он был построен в XIII веке и является одним из старейших сооружений в Калининграде. Собор был построен в готическом стиле.' },
        { id: 'img22', imageUrl: 'src/components/icons/vrangel.png', title: 'Крепость Врангеля - исторический комплекс в Калининграде, построенный в конце 19 века для защиты города и порта Кёнигсберг. Она была названа в честь генерала Петра Николаевича Врангеля. ' },
        { id: 'img23', imageUrl: 'src/components/icons/fort5.png', title: 'Форт № 5, также известный как Форт Короля Фридриха-Вильгельма III, был построен в 1843 году в рамках укреплений города Кёнигсберг (современный Калининград). Он был назван в честь короля Пруссии Фридриха Вильгельма III, который правил с 1797 по 1840 год. Король Фридрих Вильгельм III был известен своей консервативной политикой и поддержкой традиционных ценностей. Он был активным сторонником реформ, которые должны были модернизировать прусскую армию и государственное управление. Он также известен своей поддержкой искусств и культуры, в частности, покровительством композитора Людвига ван Бетховена.' },
        { id: 'img24', imageUrl: 'src/components/icons/vilage.png', title: 'Рыбацкая деревня в Калининграде - это исторический район города, который был основан рыбаками в средние века. Он расположен на берегу залива Калининградской бухты. ' },
      ],
      modalVisible: false,
      modalText: '',
      slides: [
        { text: 'src/components/SwiperIMG/Group 21.png', modalText: 'В 1255 году Калининград был известен как Кёнигсберг и был частью Тевтонского ордена. В это время город был небольшим поселением, но имел стратегическое значение из-за своего расположения на берегу Балтийского моря. В 1255 году был основан Кёнигсбергский замок, который стал центром власти Тевтонского ордена в регионе. В дальнейшем город стал важным торговым и культурным центром, а также столицей Восточной Пруссии.' },
        { text: 'src/components/SwiperIMG/Group 22.png', modalText: 'В 1701 году Калининград был известен как Кёнигсберг и был столицей герцогства Пруссия. В это время город был важным торговым и культурным центром, а также имел стратегическое значение из-за своего расположения на берегу Балтийского моря. В 1701 году герцог Пруссии Фридрих I провозгласил себя королем Пруссии, и Кёнигсберг стал столицей новообразованного королевства. В дальнейшем город стал важным центром науки и образования, а также родиной многих известных ученых и философов, таких как Иммануил Кант.' },
        { text: 'src/components/SwiperIMG/Group 23.png', modalText: 'В 1945 году Калининград был известен как Кёнигсберг и был частью нацистской Германии. В это время город был важным военно-морской базой и имел стратегическое значение для Германии. В 1945 году Кёнигсберг был захвачен советскими войсками в ходе Восточно-Прусской операции, и большая часть города была разрушена. ' },
        { text: 'src/components/SwiperIMG/Group 20.png', modalText: 'В 1946 году Калининград был переименован из Кёнигсберга в честь советского лидера Михаила Калинина. Город был разрушен в ходе Второй мировой войны, и после ее окончания он был передан Советскому Союзу.' },
        { text: 'src/components/SwiperIMG/Group 19.png', modalText: 'Калининград в 1991 году был частью Советского Союза. В этом году произошло несколько важных событий, включая распад Советского Союза и провозглашение независимости Российской Федерации. Калининград был одним из крупнейших портов в России и имел стратегическое значение для страны. В 1991 году Калининград также стал частью новообразованного Калининградского региона, который был отделен от остальной части России и окружен странами Балтии.' },
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
  <div>
    <section class="section-one">
.
      <div class="nav">
        <a>История</a>
        <a>Достопремичательности</a>
        <a>Контакты</a>
      </div>
      <p>Горд - где море встречается с историей!</p>
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
          <img src="./components/icons/beach-one.png" alt="" class="BEACHES">
          <p>Калининград находиться на берегу балтийского моря. <br>
            Мягкие песчаные пляжи, бодрящая вода и свежий <br>
            морской бриз создают идеальные условия для отдыха и туризма</p>
        </div>
        <img src="./components/icons/bigMap.svg" alt="" class="bigmap">
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
    <div
      v-for="(content, index) in contents"
      :key="index"
      class="content"
      :id="content.id"
      @mouseover="hover = index"
      @mouseleave="hover = null"
    >
      <div class="content-image" :style="{ opacity: hover === index ? 0.5 : 1 }">
        <img :src="content.imageUrl" alt="Card Image">
      </div>
      <div class="content-text" :style="{ opacity: hover === index ? 1 : 0 }">
        <p>{{ content.title }}</p>
      </div>
    </div>
  </div>
      <!-- <div class="contentiner">
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
      </div> -->
    </section>
    <section class="section-five">
       <h1>Лента времени</h1>
    <!--  <swiper  @slideChange="2" :slidesPerView="4" :spaceBetween="30" :centeredSlides="true"  :pagination="{
        clickable: true,
      }" :modules="modules" class="mySwiper">
        <swiper-slide>
          <img src="./components/SwiperIMG/Group 19.png" alt="">
        </swiper-slide>
        <swiper-slide>
          <img src="./components/SwiperIMG/Group 20.png" alt="">
        </swiper-slide>
        <swiper-slide>
          <img src="./components/SwiperIMG/Group 21.png" alt="">
        </swiper-slide>
        <swiper-slide>
          <img src="./components/SwiperIMG/Group 22.png" alt="">
        </swiper-slide>
        <swiper-slide>
          <img src="./components/SwiperIMG/Group 23.png" alt="">
        </swiper-slide>
      </swiper> -->
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
    </section>
  </div>
  <section class="section-six">
    <div class="contetet">
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
  </div>
  <img src="./components/icons/pngwing 1.png" alt="" class="lasther">
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
.nav{
display: flex;
margin: 40rem;
color: white;
margin: 3rem 40rem 0rem 45rem;
width: 31.4375rem;
/* верх:  */
/* право:*/
/* низ:   */
/* лево: */
}
.section-one {
  background: url("./components/icons/mainPage.png");
  background-repeat: no-repeat;
  height: 100vh;
}
.section-one p{
  font-family: "Fira Code";
  color: white;
  font-weight: bold;
  font-size: 2.5rem;
  margin: 38rem 30rem;
  width: 60rem;
  height: 3.25rem;
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
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.section-four .contentiner{
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.section-four .contentiner .content{
  position: relative;
  width: 19.375rem;
  height: 28.25rem;
  overflow: hidden;
}

.content-image {
  width: 100%;
  height: 100%;
  transition: opacity 0.3s ease;
}

.content-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.content-text {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  background-color: rgba(0, 0, 0, 0.7);
  transition: opacity 0.3s ease;
}

.content-text h5 {
  margin-top: 0; /* Убираем верхний отступ, чтобы текст был по центру */
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
  z-index: 1000;
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



.section-six {
  display: flex;
  width: 75rem;
  height: 29.875rem;
  border-radius: 2.1875rem;
  background: linear-gradient(to right, #FD6A21, #FB9E40);
  padding-top: 2.5rem;
  padding-left: 6.875rem;
  color: white;
}

.lasther{ 
    position: absolute;
    margin-left: 43rem;
    margin-bottom: 10rem;}

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

@media (max-width: 1366px){

  h1,
h2 {
  font-size: 2rem;

  font-weight: 300;
}

p {
  font-family: "DM Sans", sans-serif;
  font-size: .8rem;
}


.section-one{
  height: 81vh;
  background: url("./components/icons/mobile/Group 10 .png");
  background-repeat: no-repeat;
}

.section-one p {
    font-size: 2rem;
    margin: 27rem 20rem;
}

.nav{
  margin: 2rem 20rem 0rem 25rem;
}

.section-two .container h2{
    margin-left: 31.9rem;
}

.section-two .container-two p{
    margin-top: 3.3rem;
}

.section-two .museum {
  width: 15rem;
  margin-left: 24rem;
  margin-top: 10rem;
}

.section-two .sobor {
  width: 19rem;
  margin-left: 35rem;
  margin-top: 3.125rem;
}

.section-two .miniMap {
  width: 50rem;
}

.section-two .conteiner-three p{
    margin-left: 19rem;
}

.bigmap{
  width: 33rem;
}

.BEACHES{
  width: 15rem;
}
.section-two .conteiner-four .conrainer-five p{
    width: 13rem;
    margin-right: 5rem;
}
.section-two .conteiner-four .conrainer-five {
    margin-top: 5rem;
}

.section-three .container{
    gap: 4rem 0rem;
}

.section-four .contentiner{
    gap: 5rem 0rem;
}

.section-two,
.section-three,
.section-four,
.section-six,
.section-five{
  margin-top: 3.1rem;
  margin-left: 15rem;
  margin-right: 15rem;
}


.section-six{
  width: 19rem;
  padding-top: 0.5rem;
  padding-left: 1.875rem;
}
  .section-six .labeltext{
    width: 15rem;
  }

  .section-six .contei{
    margin-right: -5.625rem;
  }

.lasther{ 
display: none;
}
.section-six h4 {

  font-size: 1.5rem;

}
}

@media (max-width: 375px){

h1,
h2 {
  font-size: 1.2rem;

  font-weight: 300;
}

p {
  font-family: "DM Sans", sans-serif;
  font-size: .65rem;
}

.section-one{
height: 50vh;
background: url("./components/icons/mobile/mobminipages.png");
background-repeat: no-repeat;
}
.section-one p {
  font-size: .65rem;
  margin: 13rem 4rem;
}

.nav a{
  font-size: 2rem;
  margin: .5rem 2rem 0rem .3rem;
}
.section-two .container h2{
  margin-left: 9rem;
}
.section-two .container-two p{
  margin-top: 1.3rem;
  margin-right: 14rem;
}
.section-two .sobor {
  width: 7rem;
  margin-left: 10rem;
  margin-top: .125rem;
}
.section-two .museum {
  width: 5rem;
  margin-left: 8rem;
  margin-top: 3rem;
}
.section-two .miniMap {
  width: 22rem;
  margin-top: 3rem;
  margin-left: -5rem;
}
.section-two .conteiner-three p{
  margin-left: -1.25rem;
  margin-top: 3rem;
}

.bigmap{
  width: 22rem;
  margin-left: -26rem;
  margin-top: -24rem;
}

.BEACHES{
  width: 19rem;
}
.section-two .conteiner-four{
  margin-top: 3.75rem;
}
.section-two .conteiner-four .conrainer-five p{
  width: 19rem;
  margin-right: 6rem;
}
.section-two .conteiner-four .conrainer-five {
  margin-top: 17rem;
}

.section-three .container{
  gap: 4rem 0rem;
  width: 320px;
  margin-left: -0.25rem;
}

.section-four .contentiner{
  gap: 5rem 0rem;
}
.section-four .contentiner .content{
  position: relative;
  width: 14.375rem;
  height: 21.25rem;
}

.section-two,
.section-three,
.section-four,
.section-six,
.section-five{
  margin-top: 3.1rem;
  margin-left: 2rem;
  margin-right: 3rem;
}

.section-six{
  width: 19rem;
  padding-top: 0.5rem;
  padding-left: 1.875rem;
}
  .section-six .labeltext{
    width: 15rem;
  }

  .section-six .contei{
    margin-right: -5.625rem;
  }

}
</style>
