<template>
  <Navbar />
  <Block1 />
  <Block2 />
  <Block3 />
  <Block301 />
  <Block4 />
  <Block5 />
  <Block6 />
  <Block7 />
  <Block8 />
  <Block9 />
  <Footer />
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import Block1 from "@/components/Block1.vue";
import Block2 from "@/components/Block2.vue";
import Block3 from "@/components/Block3.vue";
import Block301 from "@/components/Block301.vue";
import Block4 from "@/components/Block4.vue";
import Block5 from "@/components/Block5.vue";
import Block6 from "@/components/Block6.vue";
import Block7 from "@/components/Block7.vue";
import Block8 from "@/components/Block8.vue";
import Block9 from "@/components/Block9.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Block1,
    Block2,
    Block3,
    Block301,
    Block4,
    Block5,
    Block6,
    Block7,
    Block8,
    Block9,
    Footer,
  },
  mounted() {
    const app = document.querySelector("#app");
    setTimeout(() => {
      app.classList.add("show");
    }, 1000);
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700;900&display=swap");

html.hidden {
  overflow: hidden;
}

body {
  margin: 0;
  font-family: "Montserrat", sans-serif;
  background: black;
}

input {
  font-family: "Montserrat", sans-serif;
}

#app {
  transition: 1s;
}

#app.show {
  opacity: 1 !important;
}

a {
  text-decoration: none;
}

.container {
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
  position: relative;
}

@media (min-width: 575.98px) {
  .container {
    max-width: 550px;
    margin: auto;
    padding: 0;
  }
}
@media (min-width: 767.98px) {
  .container {
    max-width: 740px;
  }
}
@media (min-width: 991.98px) {
  .container {
    max-width: 970px;
  }
}
@media (min-width: 1199.98px) {
  .container {
    max-width: 1099px;
  }
}
@media (min-width: 1500px) {
  .container {
    max-width: 1300px;
  }
}
</style>
