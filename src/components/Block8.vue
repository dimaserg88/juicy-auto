<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="title">
          <div class="line">Отзывы</div>
          наших клиентов
        </div>
        <div class="buttons">
          <img @click="backSlide" src="@/assets/img/block8/a-back.svg" alt="" />
          <img @click="nextSlide" src="@/assets/img/block8/a-next.svg" alt="" />
        </div>
        <div ref="swiper" class="swiper-container">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                Благодарю компанию Juicy Auto за честность. Брала кредит под
                залог авто. Процент меньше чем в банке, договор был прозрачный и
                без подводных камней. Спасибо Наталье Юрьевне за честность.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/1.jpg"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Мария Захарова</div>
                  <div class="swiper-auto">Mazda cx5 2014 года</div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                Делать машину после ДТП было не целесообразно. За битую машину
                мне предлогали копейки. Ребята из данной компании выкупили по
                очень хорошей цене и сказали что ничего критичного нет.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/2.jpg"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Антон Цевменков</div>
                  <div class="swiper-auto">Ford Focus 2019 года</div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                Очень срочно нужны были деньги в связи с покупкой квартиры.
                Сотрудники вошли в положение и адекватно оценили мой автомобиль.
                Ждать не было времени. А купили ребята действительно по рынку.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/3.jpg"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Елизавета Алексеева</div>
                  <div class="swiper-auto">Volkswagen Jetta 2016 года</div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                Обратилась в компанию по выкупу авто, осталась довольной. Были
                просрочки по кредиту, ребята быстро приехали и выкупили авто,
                закрыли все просрочки и необходимые документы. Деньги получила
                сразу же.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/4.png"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Наталья Архарова</div>
                  <div class="swiper-auto">BMW X3 2017 года</div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                На моем авто висел запрет на регистрационные действия, если
                честно я понимания не имею, как при такой ситуации сотрудники
                смогли дать такую хорошую стоимость. Спасибо Вам огромное за
                помощь.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/5.jpg"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Эдуард Семенов</div>
                  <div class="swiper-auto">Volkswagen Polo 2019 года</div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="swiper-skobka">“</div>
              <div class="swiper-text">
                Начала разводиться с мужем, надо было необходимо продать авто в
                кредите. Обратилась в компанию, получила полную консультацию и
                адекватную оценку авто. Я рада, что получилось так быстро
                закрыть этот вопрос.
              </div>
              <div class="swiper-bottom">
                <img
                  src="@/assets/img/block8/reviews/6.jpg"
                  alt=""
                  class="swiper-img"
                />
                <div class="swiper-meta">
                  <div class="swiper-name">Ангелина Гришко</div>
                  <div class="swiper-auto">Mercedes E class 2012 года</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Swiper, { Autoplay } from "swiper";
Swiper.use([Autoplay]);

// swiper bundle styles
import "swiper/swiper-bundle.min.css";

// swiper core styles
import "swiper/swiper.min.css";

export default {
  name: "Block8",
  components: {},
  data() {
    return {
      swiperEl: null,
    };
  },
  methods: {
    backSlide() {
      this.swiperEl.slidePrev();
    },
    nextSlide() {
      this.swiperEl.slideNext();
    },
  },
  mounted() {
    const mySwiper = new Swiper(".swiper-container", {
      autoplay: true,
      speed: 1000,
      loop: true,
      slidesPerView: 1,
      spaceBetween: 20,
      breakpoints: {
        575.98: { slidesPerView: 2 },
        767.98: { slidesPerView: 2 },
        1199.98: { slidesPerView: 3 },
      },
    });
    this.swiperEl = this.$refs.swiper.swiper;
  },
};
</script>

<style scoped>
.section {
  padding: 100px 0;
  background-color: #010101;
  position: relative;
  overflow: hidden;
}
.section::before {
  content: "";
  background: url("../assets/img/block8/bg.svg");
  position: absolute;
  width: 1332px;
  height: 503px;
  right: 0;
  bottom: -40px;
}
.section:after {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
}
.content {
  position: relative;
  z-index: 1;
}
.title {
  color: white;
  font-weight: 900;
  text-transform: uppercase;
  font-size: 50px;
  line-height: 70px;
  max-width: 530px;
  margin-bottom: 70px;
}
.title .line {
  position: relative;
  display: inline-block;
  z-index: 1;
}
.title .line:after {
  content: "";
  position: absolute;
  background: #e00020;
  width: 93%;
  height: 17px;
  bottom: 18px;
  left: calc(50% - 47%);
  z-index: -1;
}
.buttons {
  text-align: right;
}
.buttons img {
  cursor: pointer;
  margin: 0 5px;
}
.swiper-img {
  width: 60px;
  height: 60px;
  object-fit: cover;
  border-radius: 100px;
}
.swiper-skobka {
  font-weight: 900;
  font-size: 96px;
  color: #e00020;
}
.swiper-text {
  font-size: 16px;
  line-height: 22px;
  color: #949494;
}
.swiper-bottom {
  display: flex;
  align-items: center;
  margin-top: 25px;
}
.swiper-meta {
  margin-left: 20px;
}
.swiper-name {
  font-weight: 700;
  font-size: 20px;
  line-height: 24px;
  color: #434343;
}
.swiper-auto {
  font-size: 14px;
  line-height: 17px;
  color: #434343;
  margin-top: 4px;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
}
@media (max-width: 767.98px) {
}
@media (max-width: 575.98px) {
  .title {
    font-size: 35px;
    line-height: 60px;
  }
}
</style>
