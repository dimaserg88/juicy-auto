<template>
  <section id="contacts" class="section">
    <div class="container">
      <div class="content">
        <div class="title">Контакты</div>
        <div class="blocks">
          <div class="block">
            <div class="sub-title">Телефон</div>
            <a href="tel:89775837362" class="text">8 977 583 73 62</a>
          </div>
          <div class="block">
            <div class="sub-title">E-mail</div>
            <a href="mailto:start@juicy-auto.ru" class="text"
              >start@juicy-auto.ru</a
            >
          </div>
          <div class="block">
            <div class="sub-title">Адрес</div>
            <div class="text">
              Московская область, г. Одинцово, ул. Можайское шоссе 66
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Footer",
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
  padding-top: 100px;
  padding-bottom: 30px;
  background: #0a0a0a;
  position: relative;
}
.section:before {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
}
.title {
  color: white;
  font-size: 50px;
  font-weight: 900;
}
.blocks {
  margin-top: 70px;
  display: flex;
  justify-content: space-between;
}
.block {
}
.sub-title {
  color: white;
  font-size: 18px;
  font-weight: 700;
  margin-bottom: 7px;
}
.text {
  text-decoration: none;
  color: #e00020;
  font-weight: 700;
  max-width: 320px;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
}
@media (max-width: 767.98px) {
  .blocks {
    flex-direction: column;
    margin-top: 30px;
  }
  .block {
    margin-bottom: 20px;
  }
}
@media (max-width: 575.98px) {
  .title {
    font-size: 35px;
    line-height: 60px;
  }
}
</style>
