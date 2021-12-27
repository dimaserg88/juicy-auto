<template>
  <section class="section">
    <div ref="problems" class="problems">
      <div class="problems__inner">
        <span>Запреты</span>
        <span>Юридические проблемы</span>
        <span>В Залоге</span>
        <span>Не на ходу</span>
        <span>Срочно</span>
        <span>В кредите</span>
        <span>Без документов</span>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Block2",
  methods: {
    animateMarquee(el, duration) {
      const innerEl = el.querySelector(".problems__inner");
      const innerWidth = innerEl.offsetWidth;
      const cloneEl = innerEl.cloneNode(true);
      el.appendChild(cloneEl);

      let start = performance.now();
      let progress;
      let translateX;

      requestAnimationFrame(function step(now) {
        progress = (now - start) / duration;

        if (progress > 1) {
          progress %= 1;
          start = now;
        }

        translateX = innerWidth * progress;

        innerEl.style.transform = `translate3d(-${translateX}px, 0 , 0)`;
        cloneEl.style.transform = `translate3d(-${translateX}px, 0 , 0)`;
        requestAnimationFrame(step);
      });
    },
  },
  mounted() {
    this.animateMarquee(this.$refs.problems, 30000);
  },
};
</script>
<style scoped>
.problems {
  background: #e00020;
  overflow: hidden;
  font-size: 0;
  font-family: sans-serif;
  text-transform: uppercase;
  white-space: nowrap;
  cursor: default;
  user-select: none;
}
.problems__inner {
  white-space: nowrap;
  display: inline-flex;
}
.problems span {
  color: white;
  font-weight: 900;
  font-size: 50px;
  letter-spacing: 7px;
  text-transform: uppercase;
  margin: 0 30px;
  text-shadow: 5px 3px 1px #e00020;
}
.section {
  overflow: hidden;
  /* background: rgb(10 10 10); */
  position: relative;
  /* padding: 20px 0; */
}
.section:before {
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: url("../assets/img/block1/mask_bg.svg");
}
@media (max-width: 767.98px) {
  .problems span {
    font-size: 30px;
  }
}
</style>