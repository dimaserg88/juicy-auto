<template>
  <section class="section">
    <div ref="scene" id="scene">
      <div data-depth="0.1">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
      <div data-depth="-0.2">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
      <div data-depth="0.3">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
      <div data-depth="-0.4">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
      <div data-depth="-0.5">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
      <div data-depth="0.2">
        <img src="@/assets/img/block3/treug.svg" alt="" />
      </div>
    </div>
    <div class="container">
      <div class="content">
        <div class="sub-title">Условия</div>
        <div class="title">
          <div class="line">Все прозрачно</div>
        </div>
        <div class="blocks">
          <div class="block">
            <div class="item">
              <img
                src="@/assets/img/block3/item1.svg"
                alt=""
                class="item__img"
              />
              <div class="item__title">Связываемся</div>
              <div class="item__text">
                Вы звоните или пишите нам, либо оставляете заявку на нашем сайте
              </div>
            </div>
            <div class="item">
              <img
                src="@/assets/img/block3/item2.svg"
                alt=""
                class="item__img"
              />
              <div class="item__title">Оцениваем</div>
              <div class="item__text">
                Предварительная оценка проводится дистанционно по фото, или
                видео
              </div>
            </div>
            <div class="item">
              <img
                src="@/assets/img/block3/item3.svg"
                alt=""
                class="item__img"
              />
              <div class="item__title">Встречаемся</div>
              <div class="item__text">
                Проводим заключительный осмотр автомобиля и принимаем решение
              </div>
            </div>
            <div class="item">
              <img
                src="@/assets/img/block3/item4.svg"
                alt=""
                class="item__img"
              />
              <div class="item__title">Проводим сделку</div>
              <div class="item__text">
                Передаем Вам денежные средства, заключаем договор купли продажи
              </div>
            </div>
          </div>
          <div class="block">
            <div class="zapret">Запрет</div>
            <img class="car-img" src="@/assets/img/block3/car.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Parallax from "@/assets/js/parallax.js";

export default {
  name: "Block3",
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {
    const parallaxInstance = new Parallax(this.$refs.scene, {
      relativeInput: true,
    });
  },
};
</script>

<style scoped>
#scene {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
#scene div img {
  position: absolute;
}
#scene div:nth-child(1) img {
  left: 10vw;
  top: 100px;
  width: 45px;
}
#scene div:nth-child(2) img {
  left: 75vw;
  top: 300px;
  transform: rotate(45deg);
  width: 60px;
}
#scene div:nth-child(3) img {
  left: 50vw;
  top: 500px;
}
#scene div:nth-child(4) img {
  left: 40vw;
  top: 700px;
  width: 40px;
}
#scene div:nth-child(5) img {
  left: 20vw;
  top: 300px;
  transform: rotate(20deg);
  width: 30px;
}
#scene div:nth-child(6) img {
  left: 90vw;
  top: 100px;
  transform: rotate(70deg);
  width: 40px;
}
.section {
  padding: 100px 0;
  background: #0a0a0a;
  position: relative;
  overflow: hidden;
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
  color: #e00020;
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
.blocks {
  margin-top: 100px;
  display: flex;
  align-items: flex-end;
}
.blocks .block {
  width: 50%;
}
.blocks .block:nth-child(1) {
  display: flex;
  flex-wrap: wrap;
}
.item {
  margin: 10px;
  max-width: 170px;
  width: 100%;
  text-align: center;
  background: #0a0a0a;
  box-shadow: 0px 0px 10px 0px black;
  padding: 25px;
  transition: 0.5s;
  border-radius: 10px;
}
.item__title {
  font-weight: 900;
  color: white;
  font-size: 16px;
  line-height: 20px;
  margin: 14px 0;
  transition: 0.5s;
}
.item__text {
  font-size: 13px;
  line-height: 20px;
  color: #4b4b4b;
  transition: 0.5s;
}
.item:hover {
  background: white;
}
.item:hover .item__title {
  color: #0a0a0a;
}
.item:hover .item__text {
  color: #0a0a0a;
}
.car-img {
  width: 100%;
  position: relative;
}
.zapret {
  border: 1px solid #e00020;
  color: #e00020;
  font-size: 80px;
  text-align: center;
  text-transform: uppercase;
  font-weight: 100;
  position: absolute;
  width: 415px;
  transform: rotate(23deg);
  right: 0;
  top: 410px;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
  .blocks .block:nth-child(1) {
    position: relative;
    z-index: 1;
    width: 100%;
    justify-content: space-between;
  }
  .blocks .block:nth-child(2) {
    position: absolute;
    top: 570px;
    right: 0;
  }
  .zapret {
    font-size: 45px;
    width: 250px;
    top: -10px;
  }
}
@media (max-width: 767.98px) {
  .blocks {
    margin-top: 60px;
  }
  .item {
    max-width: calc(50% - 70px);
  }
  .blocks .block:nth-child(2) {
    display: none;
  }
}
@media (max-width: 575.98px) {
  .title {
    font-size: 35px;
    line-height: 60px;
  }
  .item {
    max-width: 100%;
  }
}
</style>
