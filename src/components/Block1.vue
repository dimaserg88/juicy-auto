<template>
  <section class="section">
    <marquee class="bg-text-1">Juicy</marquee>
    <marquee class="bg-text-2" direction="right">Auto</marquee>
    <div class="ugol-top-left" :class="isUgl ? 'show' : ''"></div>
    <div class="ugol-bottom-right" :class="isUgl ? 'show' : ''"></div>
    <div class="line-horizontal"></div>
    <div class="line-vertical"></div>
    <div class="bg-text-job">Работаем с 2017 года</div>
    <div class="circle">
      <div class="circle-1"></div>
      <div class="circle-2"></div>
      <div class="circle-3"></div>
      <div class="circle-4"></div>
      <div class="circle-5"></div>
    </div>
    <div class="container">
      <div class="content">
        <div class="block">
          <div class="sub-title">Выкупаем по рыночной стоимости</div>
          <h1 class="title">
            <div class="line">Выкуп</div>
            <div>любого</div>
            <div>автомобиля</div>
          </h1>
          <a
            href="https://api.whatsapp.com/send/?phone=79775837362"
            class="btn-max"
          >
            <span>Оценить</span>
            <img src="@/assets/img/arrow-right.svg" alt="" />
          </a>
        </div>
        <div class="block">
          <div ref="scene" id="scene">
            <div data-depth="0.1">
              <img src="@/assets/img/block1/usd.svg" alt="" />
            </div>
            <div data-depth="-0.2">
              <img src="@/assets/img/block1/usd.svg" alt="" />
            </div>
            <div data-depth="0.3">
              <img src="@/assets/img/block1/usd.svg" alt="" />
            </div>
            <div data-depth="-0.4">
              <img src="@/assets/img/block1/usd.svg" alt="" />
            </div>
            <div data-depth="0.5">
              <img src="@/assets/img/block1/usd.svg" alt="" />
            </div>
          </div>
          <div class="mercedes">
            <img
              :style="isCarShow ? 'opacity: 1' : 'opacity: 0'"
              class="primary"
              src="@/assets/img/block1/mercedes.png"
            />
            <img
              class="fara"
              :style="isFara ? 'opacity: 1' : 'opacity: 0'"
              src="@/assets/img/block1/mercedes_fara.png"
            />
            <svg
              :style="isCarSvg ? 'opacity: 1' : 'opacity: 0'"
              viewBox="0 0 1433.3333 592"
              width="1433.333251953125"
              height="592"
            >
              <path
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                  fill-opacity: 1;
                "
                d="M 809.30691,254.42759 C 679.90047,269.45249 675.8395,539.36358 814.08643,532.22066 971.89101,513.56044 925.18346,241.02368 809.30691,254.42759 Z"
                class="svg-elem-1"
              ></path>
              <path
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                d="m 1320.158,245.15806 c -40.5094,13.94236 -32.6882,177.23549 11.2185,178.50674 38.3301,-14.60794 35.4965,-187.35138 -11.2185,-178.50674 z"
                class="svg-elem-2"
              ></path>

              <path
                d="m 966.85669,133.45609 c 23.25924,-30.05198 51.55301,-137.019711 160.05401,-90.52616 12.5642,29.211945 28.4569,57.59175 31.7308,89.12627 z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-3"
              ></path>
              <path
                d="m 1249.6343,130.18968 c -29.316,3.38492 -57.4738,1.55826 -85.9765,1.28323 -7.3739,-30.04412 -18.3932,-59.567466 -34.4723,-88.367993 37.4884,17.242779 76.8242,42.667051 120.4488,87.084763 z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-4"
              ></path>
              <path
                d="m 900.12272,115.48495 c 25.61339,-9.95572 40.3868,-32.783906 56.42265,-54.112946 11.9515,-15.350631 19.01543,-32.138782 37.6151,-45.534067 C 877.24282,11.510699 760.62817,10.970942 646.16545,37.330374 588.33089,60.418064 524.75049,97.870376 463.59659,129.25642 608.18772,116.40774 754.37342,117.91009 900.12272,115.48495 Z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-5"
              ></path>
              <path
                d="m 53.453036,249.11754 c 105.109524,-8.15608 208.794194,-2.06364 312.716764,1.64979 22.79308,2.6711 23.18004,32.2781 9.48625,61.4545 -17.48851,36.4201 -43.6855,50.2875 -73.25045,55.43277 L 165.65354,380.30319 C 134.54489,373.9956 103.43625,369.11964 72.3276,356.9717 60.723459,353.05309 48.814807,337.58505 46.429654,330.84044 40.621001,309.69837 25.490196,260.18399 53.453036,249.11754 Z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-6"
              ></path>
              <path
                d="m 376.57015,292.57681 -141.38879,-2.79978 c -33.12977,-47.87989 -76.68181,-26.23595 -92.39268,-1.39989 l -80.726933,-0.93326 c -8.241895,3.60039 -12.09187,8.76933 -16.098724,13.88224 -0.595723,0.9934 -0.253869,1.36174 0.05833,1.74986 l 88.834627,7.23276 -0.69995,9.79922 -69.994448,-7.46607 -14.698835,0.23331 c -0.47635,0.5319 -1.724224,0.0718 -0.174986,3.20808 l 84.634959,11.02413 c 9.0875,54.83458 51.68173,38.78925 65.37131,1.85973 l 160.35911,-4.78438 c 2.73756,-1.53066 3.8437,-2.75543 1.31983,-3.29957 l -143.20134,2.3097 1.31983,-7.75399 150.79035,-5.77425 c 3.79406,-5.69595 7.22107,-11.39189 6.68834,-17.08784 z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-7"
              ></path>
              <path
                d="m 171.30956,276.7102 c -4.09141,11.32586 -4.84259,22.42904 -6.82599,33.61437 -8.78662,7.61185 -15.2939,15.70355 -22.76703,23.59192 7.86397,-3.10073 15.72795,-6.79825 23.59192,-11.21853 7.59013,5.61818 14.88407,8.86693 22.2721,12.86832 -3.82051,-8.62087 -9.98865,-16.06793 -15.01304,-24.08686 -0.11529,-11.81777 0.57159,-24.23715 -1.25796,-34.76922 z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-8"
              ></path>
              <path
                d="m 429.56278,321.37812 c 0.22793,-17.2019 13.83117,-44.85433 10.59987,-73.91036 77.68157,-17.52764 152.6613,-44.7819 234.26948,-48.17373 26.27574,-3.86852 29.44656,7.93 23.7569,25.73665 -18.69675,37.71354 -36.04975,44.8126 -53.28805,55.76274 0.80061,0.78623 -186.05244,76.55111 -215.3382,40.5847 z"
                style="
                  fill: none;
                  stroke: #e00020;
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                class="svg-elem-9"
              ></path>
              <path
                style="
                  fill: none;
                  stroke: rgb(254, 0, 0);
                  stroke-width: 1px;
                  stroke-linecap: butt;
                  stroke-linejoin: miter;
                  stroke-opacity: 1;
                "
                d="m 687.11221,529.858 -157.86117,11.2715 c -37.83507,-0.94882 -75.67014,0 -113.50521,0 C 331.54243,529.72847 244.60813,529.25105 159.03928,523.31182 125.38366,518.76434 91.728049,512.02026 58.072434,503.5144 42.987333,502.45313 28.939196,502.60166 12.17483,499.58125 7.1243637,493.93799 5.0219067,487.82851 4.5496394,481.0952 4.9090018,478.26076 5.1221711,473.08831 10.965797,471.06266 5.1175594,459.84185 16.704962,455.59529 22.16491,448.89775 L 35.248788,412.75277 C 21.529388,405.92533 -0.15191442,392.55751 3.8769949,381.67777 3.8533257,371.34331 6.3192792,355.75102 13.19828,343.15529 12.444718,329.60745 17.991203,316.45336 38.275013,304.22036 27.722096,262.93367 48.19235,236.58407 70.6108,211.17249 193.93514,164.33532 321.95738,137.43187 444.23145,131.58957 510.46656,97.729922 573.23949,58.244229 645.87209,34.780492 c 57.79957,-25.9730662 397.05351,-64.999433 492.35441,1.033336 68.7753,50.234415 129.2522,104.660822 208.988,148.632142 12.4133,28.98122 20.6873,57.96245 26.0666,86.94367 -0.568,32.91334 -8.4488,62.9224 -10.0154,94.1627 -2.8318,30.20446 -15.7259,65.76774 -31.5592,71.31074 -23.2639,4.78741 -58.2311,4.94899 -76.55,1.97974 -9.5916,-1.9544 -13.8418,-9.84364 -19.7975,-15.83793 L 909.92787,486.22813 C 832.08715,597.02291 731.05336,545.80339 687.11221,529.858 Z"
                class="svg-elem-10"
              ></path>
            </svg>
            <div
              @click="autoStart"
              class="btn-start-auto"
              v-show="isStartBtnShow"
              :style="
                isStartAuto
                  ? 'background:rgb(15 15 15)'
                  : 'background: #e00020;'
              "
            >
              START
              <span>engine</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Parallax from "@/assets/js/parallax.js";
import startAuto from "@/assets/audio/start_auto.mp3";
export default {
  name: "Block1",
  components: {},
  data() {
    return {
      isFara: false,
      isUgl: false,
      isCarShow: false,
      isCarSvg: true,
      isStartAuto: false,
      isStartBtnShow: false,
    };
  },
  methods: {
    autoStart() {
      this.isStartAuto = true;
      this.isFara = true;
      let mercedes_audio = new Audio(startAuto);
      mercedes_audio.play();
      mercedes_audio.addEventListener("ended", (event) => {
        this.isFara = false;
        this.isStartAuto = false;
      });
    },
  },
  mounted() {
    const parallaxInstance = new Parallax(this.$refs.scene, {
      relativeInput: true,
    });
    setTimeout(() => {
      this.isCarShow = true;
      this.isUgl = true;
      this.isCarSvg = false;
      this.isStartBtnShow = true;
    }, 4200);
    setTimeout(() => {
      this.isFara = true;
    }, 5000);
    setTimeout(() => {
      this.isFara = false;
    }, 5400);
  },
};
</script>

<style scoped>
svg {
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
}
/***************************************************
 * Generated by SVG Artista on 11/19/2021, 3:43:01 AM
 * MIT license (https://opensource.org/licenses/MIT)
 * W. https://svgartista.net
 **************************************************/

@-webkit-keyframes animate-svg-stroke-1 {
  0% {
    stroke-dashoffset: 768.1262817382812px;
    stroke-dasharray: 768.1262817382812px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 768.1262817382812px;
  }
}

@keyframes animate-svg-stroke-1 {
  0% {
    stroke-dashoffset: 768.1262817382812px;
    stroke-dasharray: 768.1262817382812px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 768.1262817382812px;
  }
}

.svg-elem-1 {
  -webkit-animation: animate-svg-stroke-1 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2s both;
  animation: animate-svg-stroke-1 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2s both;
}

@-webkit-keyframes animate-svg-stroke-2 {
  0% {
    stroke-dashoffset: 405.81646728515625px;
    stroke-dasharray: 405.81646728515625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 405.81646728515625px;
  }
}

@keyframes animate-svg-stroke-2 {
  0% {
    stroke-dashoffset: 405.81646728515625px;
    stroke-dasharray: 405.81646728515625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 405.81646728515625px;
  }
}

.svg-elem-2 {
  -webkit-animation: animate-svg-stroke-2 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.1s both;
  animation: animate-svg-stroke-2 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.1s
    both;
}

@-webkit-keyframes animate-svg-stroke-3 {
  0% {
    stroke-dashoffset: 499.0347900390625px;
    stroke-dasharray: 499.0347900390625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 499.0347900390625px;
  }
}

@keyframes animate-svg-stroke-3 {
  0% {
    stroke-dashoffset: 499.0347900390625px;
    stroke-dasharray: 499.0347900390625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 499.0347900390625px;
  }
}

.svg-elem-3 {
  -webkit-animation: animate-svg-stroke-3 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.2s both;
  animation: animate-svg-stroke-3 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.2s
    both;
}

@-webkit-keyframes animate-svg-stroke-4 {
  0% {
    stroke-dashoffset: 332.68798828125px;
    stroke-dasharray: 332.68798828125px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 332.68798828125px;
  }
}

@keyframes animate-svg-stroke-4 {
  0% {
    stroke-dashoffset: 332.68798828125px;
    stroke-dasharray: 332.68798828125px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 332.68798828125px;
  }
}

.svg-elem-4 {
  -webkit-animation: animate-svg-stroke-4 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.3s both;
  animation: animate-svg-stroke-4 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.3s
    both;
}

@-webkit-keyframes animate-svg-stroke-5 {
  0% {
    stroke-dashoffset: 1131.810546875px;
    stroke-dasharray: 1131.810546875px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 1131.810546875px;
  }
}

@keyframes animate-svg-stroke-5 {
  0% {
    stroke-dashoffset: 1131.810546875px;
    stroke-dasharray: 1131.810546875px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 1131.810546875px;
  }
}

.svg-elem-5 {
  -webkit-animation: animate-svg-stroke-5 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.4s both;
  animation: animate-svg-stroke-5 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.4s
    both;
}

@-webkit-keyframes animate-svg-stroke-6 {
  0% {
    stroke-dashoffset: 843.787841796875px;
    stroke-dasharray: 843.787841796875px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 843.787841796875px;
  }
}

@keyframes animate-svg-stroke-6 {
  0% {
    stroke-dashoffset: 843.787841796875px;
    stroke-dasharray: 843.787841796875px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 843.787841796875px;
  }
}

.svg-elem-6 {
  -webkit-animation: animate-svg-stroke-6 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.5s both;
  animation: animate-svg-stroke-6 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.5s
    both;
}

@-webkit-keyframes animate-svg-stroke-7 {
  0% {
    stroke-dashoffset: 1222.27001953125px;
    stroke-dasharray: 1222.27001953125px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 1222.27001953125px;
  }
}

@keyframes animate-svg-stroke-7 {
  0% {
    stroke-dashoffset: 1222.27001953125px;
    stroke-dasharray: 1222.27001953125px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 1222.27001953125px;
  }
}

.svg-elem-7 {
  -webkit-animation: animate-svg-stroke-7 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.6s both;
  animation: animate-svg-stroke-7 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.6s
    both;
}

@-webkit-keyframes animate-svg-stroke-8 {
  0% {
    stroke-dashoffset: 184.31597900390625px;
    stroke-dasharray: 184.31597900390625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 184.31597900390625px;
  }
}

@keyframes animate-svg-stroke-8 {
  0% {
    stroke-dashoffset: 184.31597900390625px;
    stroke-dasharray: 184.31597900390625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 184.31597900390625px;
  }
}

.svg-elem-8 {
  -webkit-animation: animate-svg-stroke-8 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.7s both;
  animation: animate-svg-stroke-8 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.7s
    both;
}

@-webkit-keyframes animate-svg-stroke-9 {
  0% {
    stroke-dashoffset: 667.974609375px;
    stroke-dasharray: 667.974609375px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 667.974609375px;
  }
}

@keyframes animate-svg-stroke-9 {
  0% {
    stroke-dashoffset: 667.974609375px;
    stroke-dasharray: 667.974609375px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 667.974609375px;
  }
}

.svg-elem-9 {
  -webkit-animation: animate-svg-stroke-9 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.8s both;
  animation: animate-svg-stroke-9 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.8s
    both;
}

@-webkit-keyframes animate-svg-stroke-10 {
  0% {
    stroke-dashoffset: 3336.06884765625px;
    stroke-dasharray: 3336.06884765625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 3336.06884765625px;
  }
}

@keyframes animate-svg-stroke-10 {
  0% {
    stroke-dashoffset: 3336.06884765625px;
    stroke-dasharray: 3336.06884765625px;
  }

  100% {
    stroke-dashoffset: 0;
    stroke-dasharray: 3336.06884765625px;
  }
}

.svg-elem-10 {
  -webkit-animation: animate-svg-stroke-10 1s cubic-bezier(0.165, 0.84, 0.44, 1)
    2.9s both;
  animation: animate-svg-stroke-10 1s cubic-bezier(0.165, 0.84, 0.44, 1) 2.9s
    both;
}

.section {
  overflow: hidden;
  background: rgb(29, 29, 29);
  background: radial-gradient(
    circle,
    rgba(29, 29, 29, 1) 0%,
    rgba(10, 10, 10, 1) 80%
  );
  padding-top: 100px;
  height: calc(100vh - 100px);
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
.ugol-top-left {
  position: absolute;
  width: calc(100% - 20px);
  height: calc(100% - 30px);
  border-left: 1px dashed #ffffff2b;
  border-top: 1px dashed #ffffff2b;
  left: 10px;
  top: 15px;
  transition: 1.5s;
  opacity: 0;
}
.ugol-bottom-right {
  position: absolute;
  width: calc(100% - 20px);
  height: calc(100% - 30px);
  border-right: 1px dashed #ffffff2b;
  border-bottom: 1px dashed #ffffff2b;
  right: 10px;
  bottom: 15px;
  transition: 1.5s;
  opacity: 0;
}
.ugol-bottom-right.show,
.ugol-top-left.show {
  width: 30px;
  height: 30px;
  opacity: 1;
}
.bg-text-1 {
  color: #00000035;
  font-size: 450px;
  position: absolute;
  font-weight: 900;
  text-transform: uppercase;
  top: 0;
  width: 100%;
}
.bg-text-2 {
  color: #00000035;
  font-size: 450px;
  position: absolute;
  font-weight: 900;
  text-transform: uppercase;
  bottom: -90px;
  width: 100%;
}
.line-horizontal {
  position: absolute;
  width: 100%;
  height: 1px;
  background: #ffffff08;
  top: calc(50% - 2px);
  left: 0;
}
.line-vertical {
  position: absolute;
  width: 1px;
  height: 100%;
  background: #ffffff08;
  top: 0;
  left: 50%;
}
.bg-text-job {
  color: #ffffff21;
  font-size: 11px;
  text-transform: uppercase;
  position: absolute;
  right: -100px;
  transform: rotate(90deg);
  top: calc(50% - 10px);
  letter-spacing: 0.45em;
}
.circle {
  width: 520px;
  position: absolute;
  height: 520px;
  top: calc(50% - 260px);
  left: calc(50% - 260px);
  border-radius: 100%;
  transform: scale(1.5);
  z-index: 1;
}
.circle-1 {
  width: 100%;
  position: absolute;
  height: 100%;
  border-radius: 100%;
  transform: scale(1.5);
  border: 1px dashed #e0002042;
  animation: rotation1 150s infinite linear;
}
@keyframes rotation1 {
  from {
    transform: scale(1.5) rotate(0deg);
  }
  to {
    transform: scale(1.5) rotate(359deg);
  }
}
.circle-2 {
  width: 100%;
  position: absolute;
  height: 100%;
  border-radius: 100%;
  transform: scale(1.2);
  border: 1px dashed #e0002042;
  animation: rotation2 100s infinite linear;
}
@keyframes rotation2 {
  from {
    transform: scale(1.2) rotate(359deg);
  }
  to {
    transform: scale(1.2) rotate(0deg);
  }
}
.circle-3 {
  width: 100%;
  position: absolute;
  height: 100%;
  border-radius: 100%;
  transform: scale(0.9);
  border: 1px dashed #e0002045;
  animation: rotation3 100s infinite linear;
}
@keyframes rotation3 {
  from {
    transform: scale(0.9) rotate(0deg);
  }
  to {
    transform: scale(0.9) rotate(359deg);
  }
}
.circle-4 {
  width: 100%;
  position: absolute;
  height: 100%;
  border-radius: 100%;
  transform: scale(0.6);
  border: 1px dashed #e0002021;
  animation: rotation4 50s infinite linear;
}
@keyframes rotation4 {
  from {
    transform: scale(0.6) rotate(359deg);
  }
  to {
    transform: scale(0.6) rotate(0deg);
  }
}
.circle-5 {
  width: 100%;
  position: absolute;
  height: 100%;
  border-radius: 100%;
  transform: scale(0.3);
  border: 1px dashed #e0002021;
}
.container {
  height: 100%;
  z-index: 2;
}
.content {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.block {
  position: relative;
}
.sub-title {
  text-transform: uppercase;
  font-size: 10px;
  line-height: 20px;
  letter-spacing: 0.45em;
  color: #e00020;
}
.title {
  color: white;
  font-weight: 900;
  text-transform: uppercase;
  font-size: 50px;
  line-height: 70px;
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
  left: 4px;
  z-index: -1;
}
.btn-max {
  width: 130px;
  height: 45px;
  background: #e00020;
  box-shadow: 0px 0px 25px rgba(224, 0, 32, 0.65);
  border-radius: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: 0.5s;
}
.btn-max span {
  font-size: 11px;
  text-align: right;
  letter-spacing: 0.1em;
  font-weight: 700;
  color: #ffffff;
  text-transform: uppercase;
}
.btn-max:hover {
  transform: scale(1.1);
}
.btn-max img {
  margin-left: 10px;
  transition: 0.5s;
}
.btn-max:hover img {
  transform: rotate(180deg);
}
#scene {
  position: absolute;
  width: 100%;
  height: 100%;
}
#scene div:nth-child(1) img {
  position: absolute;
  left: -120px;
  top: 240px;
}
#scene div:nth-child(2) img {
  position: absolute;
  left: 60px;
  top: 400px;
  transform: scale(2.5) rotate(30deg);
}
#scene div:nth-child(3) img {
  position: absolute;
  left: 320px;
  top: 50px;
  transform: scale(3) rotate(40deg);
}
#scene div:nth-child(4) img {
  position: absolute;
  left: 720px;
  top: 50px;
  transform: scale(1) rotate(0deg);
}
#scene div:nth-child(5) img {
  position: absolute;
  left: 720px;
  top: 400px;
  transform: scale(1.3) rotate(-20deg);
}
.mercedes {
  width: 800px;
  position: relative;
}
.mercedes .primary {
  width: 100%;
  opacity: 0;
  transition: 1s;
}
.mercedes .fara {
  position: absolute;
  width: 100%;
  left: 0;
  transition: 0.5s;
  opacity: 0;
}
.btn-start-auto {
  position: absolute;
  background: #e00020;
  color: white;
  width: 70px;
  height: 70px;
  text-align: center;
  line-height: 60px;
  border-radius: 100%;
  cursor: pointer;
  box-shadow: 0px 0px 10px 5px #0000008c;
  font-weight: 900;
  right: 75px;
  bottom: -25px;
  transition: 0.5s;
}
.btn-start-auto span {
  font-weight: 300;
  font-size: 9px;
  text-transform: uppercase;
  letter-spacing: 2px;
  position: absolute;
  bottom: -7px;
  left: 12px;
}
@media (max-width: 1500px) {
  .mercedes {
    width: 600px;
  }
  #scene div:nth-child(3) img {
    left: 200px;
    top: 10px;
  }
  #scene div:nth-child(4) img {
    left: 520px;
    top: 20px;
  }
  #scene div:nth-child(5) img {
    left: 520px;
    top: 300px;
  }
  .bg-text-1 {
    font-size: 370px;
    top: 20px;
  }
}
@media (max-width: 1199.98px) {
  .bg-text-1 {
    font-size: 300px;
    top: 20px;
  }
  .circle {
    width: 420px;
    height: 420px;
    top: calc(50% - 210px);
    left: calc(50% - 210px);
  }
  .mercedes {
    width: 500px;
  }
  #scene div:nth-child(2) img {
    left: 20px;
    top: 240px;
  }
  #scene div:nth-child(3) img {
    left: 20px;
    top: 10px;
  }
  #scene div:nth-child(4) img {
    left: 320px;
    top: 10px;
  }
  #scene div:nth-child(5) img {
    left: 320px;
    top: 250px;
  }
}
@media (max-width: 991.98px) {
  .bg-text-1 {
    font-size: 200px;
    /* top: 150px; */
  }
  .circle {
    width: 330px;
    height: 330px;
    top: calc(50% - 165px);
    left: calc(50% - 165px);
    transform: scale(2);
  }
  .block:nth-child(2) {
    margin-left: -160px;
    z-index: -1;
  }
  .section {
    height: auto;
    min-height: 500px;
    padding-top: 200px;
  }
  .btn-start-auto {
    right: 0;
    bottom: -70%;
  }
}
@media (max-width: 767.98px) {
  .bg-text-1 {
    font-size: 140px;
    top: 70px;
  }
  .circle {
    width: 240px;
    height: 240px;
    top: calc(50% - 120px);
    left: calc(50% - 120px);
    transform: scale(2.3);
  }
  .block:nth-child(2) {
    margin-left: -350px;
  }
  #scene div:nth-child(1) img {
    left: 120px;
    top: 300px;
  }
  #scene div:nth-child(2) img {
    left: 220px;
    top: 260px;
  }
  #scene div:nth-child(3) img {
    left: 370px;
    top: -100px;
  }
  #scene div:nth-child(4) img {
    left: 260px;
    top: -20px;
  }
  #scene div:nth-child(5) img {
    left: 350px;
    top: 220px;
  }
}
@media (max-width: 575.98px) {
  .ugol-top-left {
    display: none;
  }
  .ugol-bottom-right {
    bottom: 10px;
  }
  .bg-text-1 {
    font-size: 100px;
    top: 70px;
  }
  .bg-text-job {
    transform: rotate(0deg);
    left: 15px;
    top: auto;
    bottom: 15px;
  }
  .title {
    font-size: 35px;
    line-height: 60px;
  }
  .block:nth-child(2) {
    margin-left: -250px;
  }
  .btn-start-auto {
    right: 50%;
    bottom: -90%;
  }
}
</style>
