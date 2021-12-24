<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="title">
          <div class="line">Онлайн</div>
          оценка авто
        </div>
        <form action="#">
          <div class="input__wrap">
            <div class="input__icon">
              <img src="@/assets/img/car.svg" alt="" />
            </div>
            <input
              ref="inputPhone"
              v-model="markaAuto"
              type="text"
              placeholder="Марка и модель автомобиля"
            />
          </div>
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
        </form>
      </div>
    </div>
  </section>
</template>

<script>
import Inputmask from "inputmask";

export default {
  name: "Block9",
  components: {},
  data() {
    return {
      markaAuto: "",
      inputName: "",
      inputPhone: "",
      inputPhoneValid: false,
    };
  },
  methods: {
    sendForm() {
      if (this.inputPhoneValid) {
        this.axios
          .post("https://api.juicy-auto.ru/api/send", {
            inputName: this.inputName,
            inputPhone: this.inputPhone,
            markaAuto: this.markaAuto,
          })
          .then((response) => {
            if (response.data.status == "ok") {
              this.inputPhone = "";
              this.inputName = "";
              this.markaAuto = "";
            }
          });
      }
    },
  },
  mounted() {
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
  padding: 100px 0;
  background-color: #010101;
  position: relative;
  overflow: hidden;
}
.section::before {
  content: "";
  background: url("../assets/img/block9/bg.jpg");
  position: absolute;
  width: 1024px;
  height: 576px;
  right: 0;
  bottom: -50px;
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
  max-width: 430px;
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
  bottom: -45px;
}

@media (max-width: 1500px) {
}
@media (max-width: 1199.98px) {
}
@media (max-width: 991.98px) {
}
@media (max-width: 767.98px) {
  .section::before {
    right: -380px;
  }
}
@media (max-width: 575.98px) {
  .title {
    font-size: 35px;
    line-height: 60px;
  }
}
</style>
