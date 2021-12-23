<template>
  <section class="section">
    <div class="container">
      <div class="content">
        <div class="title">
          Популярные
          <div class="line">вопросы</div>
        </div>
        <div class="questions">
          <div class="question" :class="{ active: isActive[0] }">
            <div @click="openQuestion(0)" class="q__header">
              <div class="q__title">
                Даете ли Вы деньги под залог автомобиля?
              </div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[0]" class="q__response">
                Да, ситуации бывают разные. В нашей практике мы замечаем, что не
                все люди готовы прощаться со своими автомобилями. Поэтому мы
                предоставляем людям такую возможность.
              </div>
            </transition>
          </div>
          <div class="question" :class="{ active: isActive[1] }">
            <div class="q__header" @click="openQuestion(1)">
              <div class="q__title">Какой процент под залог?</div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[1]" class="q__response">
                В среднем это 8%, каждый случай уникальный и требует оценки
                специалиста. Свяжитесь с нами и мы точно все рассчитаем.
              </div>
            </transition>
          </div>
          <div class="question" :class="{ active: isActive[2] }">
            <div class="q__header" @click="openQuestion(2)">
              <div class="q__title">Как Вы оцениваете автомобили?</div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[2]" class="q__response">
                Автомобили оценивают наши эксперты. На стоимость выкупа авто
                нашей компанией влияют много факторов. Состояние авто, его
                рыночная стоимость. Мы даем гарантию максимальной и честной
                цены.
              </div>
            </transition>
          </div>
          <div class="question" :class="{ active: isActive[3] }">
            <div class="q__header" @click="openQuestion(3)">
              <div class="q__title">
                Можно ли получить деньги под залог ПТС?
              </div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[3]" class="q__response">
                Да, мы даем взаймы под залог ПТС. Условия на которых мы
                предоставляем взайм точно те же, что и под залог автомобиля.
                Более детальную информацию получите у наших экспертов.
              </div>
            </transition>
          </div>
          <div class="question" :class="{ active: isActive[4] }">
            <div class="q__header" @click="openQuestion(4)">
              <div class="q__title">
                Эксперт оценил мой авто выше моих ожиданий, в чем подвох?
              </div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[4]" class="q__response">
                Подвоха нет, Ваш автомобиль действительно в хорошем состоянии и
                без проблем, поэтому мы покупаем его по рыночной стоимости. Мы
                за честные сделки.
              </div>
            </transition>
          </div>
          <div class="question" :class="{ active: isActive[5] }">
            <div class="q__header" @click="openQuestion(5)">
              <div class="q__title">Решаете ли Вы нестандартные ситуации?</div>
              <div class="q__open">+</div>
            </div>
            <transition name="fade">
              <div v-show="isActive[5]" class="q__response">
                Да, мы работаем с разной сложности ситуациями. У нас опытные
                автоюристы и автоэксперты, которые обязательно помогут Вам. Мы
                даем бесплатные консультации, а так же рекомендации.
              </div>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Block7",
  components: {},
  data() {
    return {
      isActive: [false, false, false, false, false, false, false],
    };
  },
  methods: {
    openQuestion(index) {
      this.isActive[index] = !this.isActive[index];
    },
  },
  mounted() {},
};
</script>

<style scoped>
.section {
  padding: 130px 0;
  background-color: #010101;
  position: relative;
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
.questions {
}
.question {
  margin: 20px 0;
}
.q__header {
  display: flex;
  justify-content: space-between;
  cursor: pointer;
  align-items: center;
  padding: 10px;
  border-radius: 10px;
  transition: 0.5s;
}
.q__title {
  color: white;
  font-size: 20px;
  font-weight: 700;
  max-width: 500px;
}
.q__open {
  color: #e00020;
  background: white;
  font-weight: 700;
  font-size: 30px;
  width: 35px;
  height: 35px;
  min-width: 35px;
  min-height: 35px;
  text-align: center;
  line-height: 35px;
  border-radius: 100px;
  cursor: pointer;
  transition: 0.5s;
}
.q__response {
  color: white;
  max-width: 90%;
  margin-top: 15px;
  line-height: 25px;
  padding: 10px;
}
.active {
}
.active .q__open {
  transform: rotate(45deg);
}
.active .q__header {
  background: #ffffff17;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
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
