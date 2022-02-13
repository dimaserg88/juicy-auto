<template>
  <section class="section">
    <div ref="scene" id="scene">
      <div data-depth="0.2">
        <img src="@/assets/img/Block6/el1.png" alt="" />
      </div>
      <div data-depth="-0.1">
        <img src="@/assets/img/Block6/el2.png" alt="" />
      </div>
      <div data-depth="0.3">
        <img src="@/assets/img/Block6/el3.png" alt="" />
      </div>
      <div data-depth="-0.2">
        <img src="@/assets/img/Block6/el4.png" alt="" />
      </div>
    </div>
    <div class="container">
      <div class="content">
        <div class="blocks">
          <div class="block">
            <div class="title">
              <div class="line">Юридическая</div>
              чистота сделки
            </div>
            <div class="sub-title">
              Оставьте заявку и мы изучим Вашу ситуацию более детально. Дадим
              оперативный ответ и дальнейшие рекомендации.
            </div>
            <form action="#">
              <div class="input__wrap">
                <div class="input__icon">
                  <img src="@/assets/img/user.svg" alt="" />
                </div>
                <input v-model="inputName" type="text" placeholder="Ваше имя" />
              </div>
              <div class="input__wrap">
                <div class="input__icon">
                  <img src="@/assets/img/phone.svg" alt="" />
                </div>
                <input
                  ref="inputPhone"
                  v-model="inputPhone"
                  type="text"
                  placeholder="Ваш телефон"
                />
                <img
                  v-if="inputPhoneValid"
                  src="@/assets/img/Block6/done.svg"
                  alt=""
                  class="inputPhoneValid"
                />
              </div>
              <div
                @click="sendForm"
                class="submit"
                :style="[
                  !inputPhoneValid
                    ? {
                        background: 'black',
                        cursor: 'not-allowed',
                        color: '#484848',
                        boxShadow: '0px 0px 25px rgb(224 0 32 / 0%)',
                      }
                    : null,
                ]"
              >
                Отправить заявку
                <div v-if="!inputPhoneValid" class="submitError">
                  Кнопка станет активной, после заполнения номера телефона
                </div>
              </div>
              <div v-if="sendFormStatus" class="okSendForm">
                <div class="okSendForm__title">Спасибо за заявку!</div>
                <div class="okSendForm__text">
                  Мы перезвоним Вам в течение 30 минут
                </div>
              </div>
            </form>
          </div>
          <div class="block"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Parallax from "@/assets/js/parallax.js";
import Inputmask from "inputmask";

export default {
  name: "Block6",
  components: {},
  data() {
    return {
      inputName: "",
      inputPhone: "",
      inputPhoneValid: false,
      sendFormStatus: false,
    };
  },
  methods: {
    sendForm() {
      if (this.inputPhoneValid) {
        this.axios
          .post("https://api.juicy-auto.ru/api/send", {
            inputName: this.inputName,
            inputPhone: this.inputPhone,
          })
          .then((response) => {
            if (response.data.status == "ok") {
              this.inputPhone = "";
              this.inputName = "";
              this.sendFormStatus = true;
              setTimeout(() => (this.sendFormStatus = false), 10000);
            }
          });
      }
    },
  },
  mounted() {
    const parallaxInstance = new Parallax(this.$refs.scene, {
      relativeInput: true,
    });

    const inputPhone = new Inputmask("+7 (999) 999 99 99");
    inputPhone.mask(this.$refs.inputPhone);
  },
  watch: {
    inputPhone(val) {
      let n = val.match(/\d/g);
      n = n ? (n = n.length) : 0;
      this.inputPhoneValid = true ? n == 11 : (this.inputPhoneValid = false);
    },
  },
};
</script>

<style scoped>
.section {
  padding: 130px 0;
  background-color: #010101;
  position: relative;
  overflow: hidden;
}
.section::before {
  content: "";
  position: absolute;
  background: url("../assets/img/Block6/grek.jpg");
  width: 612px;
  height: 344px;
  right: 0;
  transform: scaleX(-1);
  bottom: 0;
}
.section:after {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
}
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
  left: 80vw;
  top: 50px;
  width: 80px;
}
#scene div:nth-child(2) img {
  left: 60vw;
  top: 180px;
  width: 140px;
}
#scene div:nth-child(3) img {
  left: 40vw;
  top: 400px;
  width: 400px;
}
#scene div:nth-child(4) img {
  left: 3vw;
  top: 150px;
  width: 190px;
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
.sub-title {
  color: white;
  margin-top: 20px;
  max-width: 390px;
  line-height: 25px;
}
form {
  margin-top: 40px;
  display: inline-block;
  background: #ffffff14;
  padding: 20px;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
}
.okSendForm {
  position: absolute;
  background: white;
  width: calc(100% - 40px);
  height: 100%;
  top: 0;
  left: 0;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.okSendForm__title {
  font-weight: 700;
  font-size: 22px;
  text-align: center;
}
.okSendForm__text {
  text-align: center;
  margin-top: 15px;
}
.input__wrap {
  max-width: 340px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  overflow: hidden;
  border-radius: 10px;
  background: #ffffff0d;
  margin: 10px 0;
  position: relative;
}
.input__icon {
  background: white;
  padding: 5px;
}
.input__icon img {
  width: 25px;
}
input {
  font-size: 16px;
  display: block;
  width: 100%;
  padding: 10px;
  background: transparent;
  border: none;
  outline: none;
  color: white;
}
input::placeholder {
  font-size: 14px;
}
.inputPhoneValid {
  position: absolute;
  width: 20px;
  right: 15px;
}
.submit {
  background: #e00020;
  color: white;
  padding: 15px;
  font-weight: 700;
  max-width: 210px;
  cursor: pointer;
  border-radius: 10px;
  margin-top: 20px;
  box-shadow: 0px 0px 25px rgb(224 0 32 / 65%);
  transition: 0.5s;
  position: relative;
}
.submitError {
  font-weight: 100;
  font-size: 13px;
  color: white;
  position: absolute;
  bottom: -60px;
}
@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
  #scene div:nth-child(3) img {
    width: 200px;
    left: 7vw;
    top: 617px;
  }
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
