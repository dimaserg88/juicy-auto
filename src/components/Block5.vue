<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="item">
          <div class="title">~ Время приезда</div>
          <div class="num">40</div>
          <div class="sub-title">минут</div>
        </div>
        <div class="item">
          <div class="title">~ Время выкупа</div>
          <div class="num">30</div>
          <div class="sub-title">минут</div>
        </div>
        <div class="item">
          <div class="title">~ Довольных</div>
          <div class="num">3670</div>
          <div class="sub-title">клиентов</div>
        </div>
        <div class="item">
          <div class="title">~ Опыт работы</div>
          <div class="num">17</div>
          <div class="sub-title">лет</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Block5",
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>

<style scoped>
.section {
  background: #e00020;
  padding: 50px 0;
  position: relative;
}
.section:before {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
  opacity: 0.3;
}
.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.item {
  background: #e00020;
  box-shadow: 0px 0px 20px 0px #00000066;
  padding: 20px;
  text-align: center;
  border-radius: 10px;
}
.title {
  font-size: 18px;
  font-weight: 900;
  color: white;
}
.num {
  font-size: 64px;
  font-weight: 900;
  color: white;
}
.sub-title {
  font-weight: 100;
  color: white;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
  .item {
    padding: 17px;
  }
  .title {
    font-size: 16px;
  }
  .num {
    font-size: 30px;
    margin: 7px 0;
  }
}
@media (max-width: 767.98px) {
  .content {
    flex-wrap: wrap;
  }
  .item {
    width: calc(50% - 60px);
    margin: 10px;
  }
}
@media (max-width: 575.98px) {
  .item {
    margin: 10px 0;
    width: 100%;
  }
}
</style>
