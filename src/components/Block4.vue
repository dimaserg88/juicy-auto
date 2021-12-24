<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="sub-title">Смотрите</div>
        <div class="title">
          <div class="line">Выкупленные авто</div>
        </div>
      </div>
    </div>
    <swiper
      :breakpoints="swiperOptions.breakpoints"
      :modules="modules"
      :slides-per-view="1"
      :space-between="20"
      loop="true"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide>
        <img
          src="https://www.a777aa77.ru/hamann/2015-bmw-x6-m50d-hamann-widebody-f16.jpg"
          alt=""
          class="swiper-img"
        />
        <div class="swiper-title">BMW X6 2015</div>
        <div class="swiper-price">2.450.000 Р</div>
      </swiper-slide>
      <swiper-slide>
        <img
          src="https://www.a777aa77.ru/hamann/2015-bmw-x6-m50d-hamann-widebody-f16.jpg"
          alt=""
          class="swiper-img"
        />
        <div class="swiper-title">BMW X6 2015</div>
        <div class="swiper-price">2.450.000 Р</div>
      </swiper-slide>
      <swiper-slide>
        <img
          src="https://www.a777aa77.ru/hamann/2015-bmw-x6-m50d-hamann-widebody-f16.jpg"
          alt=""
          class="swiper-img"
        />
        <div class="swiper-title">BMW X6 2015</div>
        <div class="swiper-price">2.450.000 Р</div>
      </swiper-slide>
      <swiper-slide>
        <img
          src="https://www.a777aa77.ru/hamann/2015-bmw-x6-m50d-hamann-widebody-f16.jpg"
          alt=""
          class="swiper-img"
        />
        <div class="swiper-title">BMW X6 2015</div>
        <div class="swiper-price">2.450.000 Р</div>
      </swiper-slide>
      <swiper-slide>
        <img
          src="https://www.a777aa77.ru/hamann/2015-bmw-x6-m50d-hamann-widebody-f16.jpg"
          alt=""
          class="swiper-img"
        />
        <div class="swiper-title">BMW X6 2015</div>
        <div class="swiper-price">2.450.000 Р</div>
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
// swiper bundle styles
import "swiper/swiper-bundle.min.css";

// swiper core styles
import "swiper/swiper.min.css";

export default {
  name: "Block4",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {};
  },
  methods: {},
  setup() {
    const onSwiper = (swiper) => {};
    const onSlideChange = () => {};
    return {
      onSwiper,
      onSlideChange,
      modules: [],
      swiperOptions: {
        breakpoints: {
          575.98: { slidesPerView: 2 },
          767.98: { slidesPerView: 3 },
          1199.98: { slidesPerView: 4 },
        },
      },
    };
  },
};
</script>

<style scoped>
.section {
  padding: 100px 0;
  background: #0a0a0a;
  position: relative;
}
.section:after {
  content: "";
  background: url(../assets/img/block4/bg.jpg);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-size: cover;
  opacity: 0.1;
  background-position: 0px 0px;
  background-repeat: no-repeat;
}
.section:before {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
}
.sub-title {
  text-transform: uppercase;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.45em;
  color: white;
  text-align: center;
}
.title {
  margin-top: 40px;
  margin-bottom: 30px;
  color: white;
  font-weight: 900;
  text-transform: uppercase;
  font-size: 50px;
  line-height: 70px;
  text-align: center;
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
.swiper-container {
  padding: 20px 0;
}
.swiper-slide {
  background: #0a0a0a;
  box-shadow: 0px 0px 20px 0px #000000b0;
  overflow: hidden;
  border-radius: 10px;
}
.swiper-img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transform: scale(1);
  transition: 0.5s;
}
.swiper-slide:hover .swiper-img {
  transform: scale(1.1);
}
.swiper-title {
  font-weight: 700;
  padding: 10px;
  color: #e00020;
  text-align: center;
  font-size: 20px;
}
.swiper-price {
  text-align: center;
  font-size: 14px;
  padding: 10px;
  font-weight: 700;
  padding-top: 0;
  color: white;
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
  .swiper-img {
    height: auto;
  }
}
</style>
