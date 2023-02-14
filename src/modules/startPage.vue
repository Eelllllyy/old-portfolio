<template>
<section class="section" @mousemove="playParallax">
  <div class="flower one" name="img"></div>
  <div class="flower two" name="img"></div>
  <div class="flower three" name="img"></div>
  <div class="flower four" name="img"></div>
  <div class="flower five" name="img"></div>
  <div class="flower six" name="img"></div>
  <div class="flower seven" name="img"></div>
  <div class="flower eight" name="img"></div>
  <div class="flower nine" name="img"></div>
  <div class="flower ten" name="img"></div>
  <div class="flower eleven" name="img"></div>
  <div class="flower twelve" name="img"></div>
  <div class="flower thirteen" name="img"></div>
  <div class="flower fourteen" name="img"></div>

  <h1 class="header center greetings" id="headerGreetings">Привет!</h1>
  <h1 class="header center name" id="headerName">Меня зовут Элина</h1>
  <h1 class="header center about" id="headerAbout">Я Frontend разработчик</h1>
  <h1 class="header center portfolio" id="headerPortfolio">И вот мое портфолио!</h1>

  <main class="main">
    <article class="feature bottom-double grid ">
      <div class="image-container ipsGrid_span5 reveal reveal_fromLeft">
        <div class="card">
          <img width="479" src="../assets/images/avatar.png" alt="">
        </div>
      </div>
      <div class="ipsGrid_span7 type_left reveal text list">
        <h2 class="heading-large"></h2>
        <ul class="ident">
          <li><a href="https://t.me/eelllllyy">
             <font-awesome-icon icon="fa-brands fa-telegram"/> Telegram
          </a></li>
          <li><a href="https://hh.ru/applicant/resumes/view?resume=222787aaff0bb781a30039ed1f534877545331
"><span class="hh">hh</span> HeadHunter</a></li>
          <li><a href="https://github.com/Eelllllyy">
            <font-awesome-icon icon="fa-brands fa-github" /> GitHub
          </a></li>
          <li><a href="https://www.linkedin.com/in/%D1%8D%D0%BB%D0%B8%D0%BD%D0%B0-%D1%80%D0%B5%D0%B7%D0%B5%D0%BD%D1%8C%D0%BA%D0%BE%D0%B2%D0%B0-743b9b258/">
            <font-awesome-icon icon="fa-brands fa-linkedin" /> Linkedin
          </a></li>
          <li><a href="mailto:r-elina-r@yandex.ru">
            <font-awesome-icon icon="fa-regular fa-envelope" /> E-mail
          </a> </li>
        </ul>
      </div>
    </article>

    <article class="feature bottom-double grid">
      <div class="ipsGrid_span7 type_right reveal text">
        <h2 class="heading-large">Nasa portal</h2>
        <p>Корпоративный портал для сотрудников, в котором реализована аутентификация с помощью JWT, а так же восстановление пароля через почту. На данном портале есть возможность оставить заявку на различные услуги, начиная от обращения к шефу и заканчивая заявлением на отпуск.</p> 
        <p>Можно просматривать список сотрудников, который я реализовала в двух вариациях:</p>
          <ul class="ident">
            <li>1. С обычной пагинацией;</li>
            <li>2. С пагинацией в виде инфинити скролл.</li>
          </ul>
        <p>Каждого сотрудника можно отредактировать или удалить.</p>
        <p>Проект реализован с помощью Vue 3,  composition API , vue-router, pinia</p>
        <a href="https://github.com/Eelllllyy/nasa-portal">
            <font-awesome-icon icon="fa-brands fa-github" /> GitHub
        </a>
      </div>
      <a href="https://github.com/Eelllllyy/nasa-portal">
        <div class="image-container ipsGrid_span5 reveal reveal_fromRight">
        <div class="card">
          <img width="479" src="../assets/images/nasa_portal.png" alt="">
        </div>
      </div>
      </a>

    </article>

    <article class="feature bottom-double grid">
      <a href="https://github.com/Eelllllyy/minos">
        <div class="image-container ipsGrid_span5 reveal reveal_fromLeft">
        <div class="card">
          <img width="479" src="../assets/images/minos.png" alt="">
        </div>
      </div>
      </a>
      <div class="ipsGrid_span7 type_left reveal text">
        <h2 class="heading-large">Minos</h2>
        <p>Лендинг игры в телеграмме с кроссбраузерной версткой.</p>
        <p>Проект реализован с помощью Vue 3, composition API, swiper</p>
        <a href="https://github.com/Eelllllyy/minos">
            <font-awesome-icon icon="fa-brands fa-github" /> GitHub
        </a>
      </div>
    </article>

    <article class="feature bottom-double grid">
      <div class="ipsGrid_span7 type_right reveal text">
        <h2 class="heading-large">Airbnb clone</h2>
        <p>Клон сайта для размещения и поиска краткосрочной аренды — airbnb.</p>
        <p>В данном проекте я реализовала аутентификацию и регистрацию пользователя, возможность просмотра списка и отдельного объявления, полнотекстового поиска и пагинации.</p>
        <p>Проект реализован с помощью Vue 3,  composition API , vue-router, pinia, swiper</p>
        <a href="https://github.com/Eelllllyy/airbnb-clone">
            <font-awesome-icon icon="fa-brands fa-github" /> GitHub
        </a>
      </div>
      <a href="https://github.com/Eelllllyy/airbnb-clone">
        <div class="image-container ipsGrid_span5 reveal reveal_fromRight">
          <div class="card">
            <img width="479" src="../assets/images/airbnb_clone.png" alt="">
          </div>
      </div>
      </a>
    </article>

    <article class="feature grid">
      <a href="https://github.com/Eelllllyy/cards">
        <div class="image-container ipsGrid_span5 reveal reveal_fromLeft">
        <div class="card">
          <img width="479" src="../assets/images/card.png" alt="">
        </div>
      </div>
      </a>
      <div class="ipsGrid_span7 type_left text reveal">
        <h2 class="heading-large">Cards</h2>
        <p>Интерактивный проект-игра с аутентификацией по секретному коду, основная задумка которого заключалась в том, чтобы при помощи интеграции с телеграмм ботом открывать карточки с изображениями, которые в последующем преобразуются в одну единую картинку.</p>
        <p>Проект реализован с помощью Vue 3,  composition API , vue-router, WebSocket</p>
        <a href="https://github.com/Eelllllyy/cards">
            <font-awesome-icon icon="fa-brands fa-github" /> GitHub
        </a>
      </div>
    </article>
  </main>
</section>
</template>
<script setup>
import { onMounted } from "vue";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
onMounted(() => {
  gsap.fromTo(
    "#headerGreetings",
    {
      opacity: 0,
      x: "-100%",
    },
    {
      duration: 1.9,
      opacity: 1,
      x: 0,
      delay: 0.2,
      ease: "power3.inOut"
    }
  );
    gsap.fromTo(
    "#headerName",
    {
      opacity: 0,
      x: "-100%",
    },
    {
      duration: 1.9,
      opacity: 1,
      x: 0,
      delay: 0.7,
      ease: "power3.inOut"
    }
  );
    gsap.fromTo(
    "#headerAbout",
    {
      opacity: 0,
      x: "-100%",
    },
    {
      duration: 1.9,
      opacity: 1,
      x: 0,
      delay: 1.2,
      ease: "power3.inOut"
    }
  );
  gsap.fromTo(
    "#headerPortfolio",
    {
      opacity: 0,
      x: "-200%",
    },
    {
      duration: 1.9,
      opacity: 1,
      x: 0,
      delay: 1.6,
      ease: "power3.inOut",
    }
  );
})
gsap.registerPlugin(ScrollTrigger);

function animateFrom(elem, direction) {
  direction = direction || 1;
  var x = 0,
      y = direction * 100;
  if(elem.classList.contains("reveal_fromLeft")) {
    x = -100;
    y = 0;
  } else if (elem.classList.contains("reveal_fromRight")) {
    x = 100;
    y = 0;
  }
  elem.style.transform = "translate(" + x + "px, " + y + "px)";
  elem.style.opacity = "0";
  gsap.fromTo(elem, {x: x, y: y, autoAlpha: 0}, {
    duration: 1.25, 
    x: 0,
    y: 0, 
    autoAlpha: 1, 
    ease: "expo", 
    overwrite: "auto"
  });
}
function hide(elem) {
  gsap.set(elem, {autoAlpha: 0});
}
document.addEventListener("DOMContentLoaded", function() {
  gsap.registerPlugin(ScrollTrigger);
  gsap.utils.toArray(".reveal").forEach(function(elem) {
    hide(elem); 
    
    ScrollTrigger.create({
      trigger: elem,
      // markers: true,
      onEnter: function() { animateFrom(elem) }, 
      onEnterBack: function() { animateFrom(elem, -1) },
      onLeave: function() { hide(elem) } 
    });
  });
});
const playParallax = (e) => {
  let imagePlx = document.getElementsByName('img');
  let x = e.clientX / window.innerWidth;
  let y = e.clientY / window.innerHeight;
  for (let i = 0; i < imagePlx.length; i++) {
    if (i % 2) {
      imagePlx[i].style.transform = 'translate(-' + x * 50 + 'px, -' + y * 50 + 'px)';
    } else {
      imagePlx[i].style.transform = 'translate(+' + x * 50 + 'px, +' + y * 50 + 'px)';
    }
  }
};
</script>
<style>
body {
  font-weight: 300;
}
.type_right {
  text-align: left;
}
.center {
  text-align: center;
}
.section {
  margin: 0 auto;
  /* background-color: #fce9f9; */
  background: linear-gradient(#fce9f9, #f8f1f7);
}
.main{
  max-width: 1240px;
  margin-left: auto;
  margin-right: auto;
}
.bottom-double {
  margin-bottom: 30px;
}
.grid {
  display: inline-block;
  display: -ms-flexbox;
  display: flex;
  /* flex-wrap: wrap; */
}
.grid::before, .grid::after {
  display: table;
  content: "";
  line-height: 0;
}
.grid > [class*="ipsGrid_span"] {
  display: block;
  width: 100%;
  min-height: 30px;
  box-sizing: border-box;
}
.grid > .ipsGrid_span5 {
  width: 40.42553191489362%;
}
.grid > .ipsGrid_span7 {
  width: 57.44680851063829%;
}
.grid > [class*="ipsGrid_span"] {
  float: left;
  margin-left: 2%;
}
.grid > [class*="ipsGrid_span"]:first-child {
  margin-left: 0;
}
.feature {
  display: flex;
  align-items: center;
  position: relative;
  z-index: 100;
}
.card {
  margin-bottom: 30px;
  border: 1px solid #cccccc;
  border-radius: 8px;
  overflow: hidden;
  background: #ffffff;
  box-shadow: 1px 1px 5px 1px #CCCCCC;
  padding-bottom: 0;
  z-index: 11;
  position: relative;
/*   transition: 0.3s; */
}
.image-container .card {
  padding: 15px;
  height: 0;
  padding-bottom: calc(100% - 10px);
}
h2.heading-large {
  font-size: 3.0em;
  padding-bottom: 10px;
}
img {
  max-width: 100%;
}

.header {
 padding:100px
}

.reveal {
  opacity: 0;
  visibility: hidden;
  will-change: transform, opacity;
}
.greetings{
  font: 300 70px/ 30px 'tatiana';
  background: linear-gradient(#9c77ec, #b999eb);
}
.name{
  font: 300 70px/ 30px 'tatiana';
  background: linear-gradient(#b999eb, #c5a3eb);
}
.about{
  font: 300 70px/ 30px 'tatiana';
  background: linear-gradient(#c5a3eb, #dfb9eb);
}
.portfolio{
  font: 300 70px/ 30px 'tatiana';
  background: linear-gradient(#dfb9eb, #fce9f9);
  margin-bottom: 100px;
}
.greetings:hover , .name:hover , .about:hover, .portfolio:hover{
  background-color: rgba(0, 0, 0, 0.116);
}
.ident{
  text-indent: 20px;
  list-style: none;
}
.text{
  font: 200 16px/ 40px 'tatiana';
  color:rgb(24, 24, 24)
}
.flower{
  background-image: url("../assets/images/star-one.svg");
  width: 30px;
  height: 30px;
  position: fixed;
  z-index: 5;
  opacity: 0.7;
}
.one{
  bottom: 44px;
  right: 250px;
}
.two{
  bottom: 134px;
  right: 150px;
}

.three{
  bottom: 364px;
  right: 80px;
}

.four{
  bottom: 440px;
  right: 250px;
}

.five{
  top: 202px;
  right: 162px;
}

.six{
  top: 102px;
  right: 403px;
}
 
.seven{
  top: 30px;
  right: 52px;
}


.eight{
  bottom: 44px;
  left: 250px;
}
.nine{
  bottom: 194px;
  left: 100px;
}
.ten{
  bottom: 364px;
  left: 80px;
} 
.eleven{
  bottom: 440px;
  left: 250px;
}
.twelve{
  top: 202px;
  left: 162px;
}
.thirteen{
  top: 102px;
  left: 403px;
} 
.fourteen{
  top: 30px;
  left: 52px;
} 
@media(max-width: 1450px){
  .about{
    font: 300 70px/ 83px 'tatiana';
  }
}
@media(max-width: 850px){
  .name, .portfolio, .greetings, .about{
    font: 300 40px/ 83px 'tatiana';
  }
  .header {
    padding: 36px;
  }
  .feature{
    flex-direction: column;
  }
  .image-container .card {
    padding: 0;
    height: 0;
    padding-bottom: calc(100% - 10px)!important;
}
.flower{
  opacity: 0;

}
}
a{
  text-decoration: none;
  color:black;
}
a:hover{
  color: blue;
}
.hh{
  border-radius: 20px;
  border: 1px solid black;
  font-size: 10px;
  padding: 3px 3px 4px 3px;
}
.list{
  font-size: 20px;
}
</style>