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
    <div ref="swiperAuto" class="swiper-container-auto">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img
            src="@/assets/img/block4/solaris2018.jpg"
            alt=""
            class="swiper-img"
          />
          <div class="swiper-title">Hyundai Solaris 2018 года</div>
          <div class="swiper-price">620.000 Р</div>
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/block4/mlamg.jpg" alt="" class="swiper-img" />
          <div class="swiper-title">Mercedes ML 63 AMG</div>
          <div class="swiper-price">1.300.000 Р</div>
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/block4/kiak5.jpg" alt="" class="swiper-img" />
          <div class="swiper-title">Kia K5 2020 года</div>
          <div class="swiper-price">1.750.000 Р</div>
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/block4/camry.jpg" alt="" class="swiper-img" />
          <div class="swiper-title">Toyota Camry 2.5 2019 года</div>
          <div class="swiper-price">1.650.000 Р</div>
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/block4/prado.jpg" alt="" class="swiper-img" />
          <div class="swiper-title">Toyota Land Cruiser Prado 2013 года</div>
          <div class="swiper-price">2.300.000 Р</div>
        </div>
        <div class="swiper-slide">
          <img
            src="@/assets/img/block4/bmw2012.jpg"
            alt=""
            class="swiper-img"
          />
          <div class="swiper-title">BMW 5 2012 года</div>
          <div class="swiper-price">1.000.000 Р</div>
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
  name: "Block4",
  components: {},
  data() {
    return {
      swiperElAuto: null,
    };
  },
  methods: {},
  mounted() {
    const mySwiperAuto = new Swiper(".swiper-container-auto", {
      autoplay: true,
      speed: 1000,
      loop: true,
      slidesPerView: 1,
      spaceBetween: 20,
      breakpoints: {
        575.98: { slidesPerView: 2 },
        767.98: { slidesPerView: 3 },
        1199.98: { slidesPerView: 3 },
      },
    });
    this.swiperElAuto = this.$refs.swiperAuto.swiper;
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
.swiper-container-auto {
  overflow: hidden;
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
  .swiper-title {
    font-size: 16px;
  }
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
