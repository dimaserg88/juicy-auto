<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="sub-title">Наши компетенции</div>
        <div class="title">
          Чем мы Вам
          <div class="line">поможем</div>
        </div>
        <div class="text">
          Мы выкупим Ваш автомобиль, с любой юридической проблемой за 1 час
        </div>
        <div class="items">
          <div class="item">
            <div class="item__title">ВЫКУП КРЕДИТНЫХ АВТО</div>
            <div class="item__text">
              Мы выкупим Ваш автомобиль, даже если он находится в собственности
              у банка
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
              </div>
              <div class="item__count">~ 310 авто</div>
            </div>
          </div>
          <div class="item">
            <div class="item__title">ВЫКУП АВТО В ЗАЛОГЕ</div>
            <div class="item__text">
              Ваш автомобиль находится в залоге? Не проблема, мы его выкупим по
              самой приятной Вам цене
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
              </div>
              <div class="item__count">~ 180 авто</div>
            </div>
          </div>
          <div class="item">
            <div class="item__title">ВЫКУП АВТО БЕЗ ПТС</div>
            <div class="item__text">
              Потеряли ПТС и нет возможности восстановить? Купим Ваш автомобиль
              без ПТС
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_yg.svg" alt="" />
              </div>
              <div class="item__count">~ 70 авто</div>
            </div>
          </div>
          <div class="item">
            <div class="item__title">ВЫКУП АВТО НА РАЗБОРКУ</div>
            <div class="item__text">
              Мы покупаем автомобили на разборку, с целью дальнейшей продажи по
              запчастям
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_yg.svg" alt="" />
              </div>
              <div class="item__count">~ 90 авто</div>
            </div>
          </div>
          <div class="item">
            <div class="item__title">ВЫКУП АВТО В АРЕСТЕ</div>
            <div class="item__text">
              Наложили арест на автомобиль? Хотите побыстрей продать? Свяжитесь
              с нами и мы поможем
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_g.svg" alt="" />
              </div>
              <div class="item__count">~ 30 авто</div>
            </div>
          </div>
          <div class="item">
            <div class="item__title">ВЫКУП АВТО С ЗАПРЕТОМ</div>
            <div class="item__text">
              На Ваш авто наложен запрет на регистрационные действия? Давайте мы
              его у Вас купим
            </div>
            <div class="item__bottom">
              <div class="item__stars">
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_y.svg" alt="" />
                <img src="@/assets/img/block301/star_yg.svg" alt="" />
              </div>
              <div class="item__count">~ 27 авто</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Block301",
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {},
  watch: {},
};
</script>

<style scoped>
.section {
  padding: 100px 0;
  background-color: #010101;
  position: relative;
  overflow: hidden;
  background-image: url("../assets/img/block301/bg.svg");
  background-size: cover;
}
/* .section::before {
  content: "";
  background: url("../assets/img/block301/bg.svg");
  position: absolute;
  width: 1583.5px;
  height: 609.5px;
  right: le;
  bottom: -50px;
} */
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
.sub-title {
  text-transform: uppercase;
  font-size: 10px;
  line-height: 20px;
  letter-spacing: 0.45em;
  color: #e00020;
  margin-bottom: 20px;
}
.title {
  color: white;
  font-weight: 900;
  text-transform: uppercase;
  font-size: 50px;
  line-height: 70px;
  max-width: 430px;
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
.text {
  color: white;
  margin-top: 20px;
  max-width: 390px;
  line-height: 25px;
}
.items {
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.item {
  background: #0a0a0a;
  box-shadow: 0px 0px 25px rgb(0 0 0 / 70%);
  padding: 25px;
  width: calc(33% - 70px);
  margin: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.item__title {
  font-weight: bold;
  font-size: 18px;
  line-height: 22px;
  color: white;
  margin-bottom: 15px;
}
.item__text {
  font-size: 14px;
  line-height: 17px;
  color: #464646;
}
.item__bottom {
  margin-top: 35px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.item__stars {
}
.item__count {
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  color: #e00020;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
  .item {
    width: calc(50% - 70px);
  }
}
@media (max-width: 767.98px) {
  .item {
    width: 100%;
    margin: 10px 0;
  }
}
@media (max-width: 575.98px) {
  .title {
    font-size: 35px;
    line-height: 60px;
  }
}
</style>
