<template>
  <header>
    <div class="container">
      <div class="content">
        <div class="block">
          <img class="logo" src="@/assets/img/logo.svg" alt="" />
        </div>
        <div class="block">
          <div
            @click="openMenu"
            class="nav-btn"
            :class="isOpenMenu ? 'active' : ''"
          >
            <span></span>
          </div>
          <ul :class="isOpenMenu ? 'active' : ''">
            <li><a href="#">главная</a></li>
            <li><a href="#">условия</a></li>
            <li><a href="#">оценка авто</a></li>
            <li><a href="#">контакты</a></li>
          </ul>
        </div>
        <div class="block">
          <a
            href="https://api.whatsapp.com/send/?phone=79775837362"
            class="btn-min"
            ><span>связаться</span></a
          >
          <div class="contacts">
            <a class="phone" href="tel:+79775837362">8 977 583 73 62</a>
            <span class="region">Московская область</span>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isOpenMenu: false,
    };
  },
  methods: {
    openMenu() {
      this.isOpenMenu = !this.isOpenMenu;
      const html = document.querySelector("html");
      if (this.isOpenMenu) {
        html.classList.add("hidden");
      } else {
        html.classList.remove("hidden");
      }
    },
  },
};
</script>

<style scoped>
header {
  padding: 20px 0;
  position: absolute;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 98;
}
.content {
  display: flex;
  align-items: center;
}
.block:nth-child(1) {
  display: flex;
}
.block:nth-child(2) {
  margin-left: 150px;
}
.block:nth-child(3) {
  margin-left: auto;
  display: flex;
  align-items: center;
}
.logo {
}
.nav-btn {
  display: none;
  width: 30px;
  height: 24px;
  position: relative;
  cursor: pointer;
  z-index: 100;
}
.nav-btn span {
  position: absolute;
  width: 100%;
  height: 2px;
  background: white;
  border-radius: 10px;
  top: calc(50% - 1px);
  transition: 0.5s;
}
.nav-btn span:before {
  content: "";
  position: absolute;
  background: white;
  width: 100%;
  height: 100%;
  top: -10px;
  transition: 0.5s;
}
.nav-btn span:after {
  content: "";
  position: absolute;
  background: white;
  width: 100%;
  height: 100%;
  top: 10px;
  transition: 0.5s;
}
.nav-btn.active span {
  transform: rotate(45deg);
}
.nav-btn.active span:before {
  opacity: 0;
}
.nav-btn.active span:after {
  transform: rotate(90deg);
  top: 0;
}
ul {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  z-index: 99;
}
ul li {
  margin: 0 15px;
  position: relative;
}
ul li:after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 0px;
  height: 1px;
  background: #e00020;
  transition: 0.5s;
}
ul li:hover::after {
  width: 100%;
}
ul li a {
  font-weight: 700;
  color: white;
  font-size: 11px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}
.btn-min {
  min-width: 130px;
  width: 130px;
  height: 45px;
  border: 1px solid #e00020;
  border-radius: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: 0.5s;
}
.btn-min span {
  font-weight: 700;
  font-size: 11px;
  letter-spacing: 0.1em;
  color: #e00020;
  text-transform: uppercase;
  transition: 0.5s;
}
.btn-min:hover {
  background: #e00020;
}
.btn-min:hover span {
  color: white;
}
.contacts {
  display: flex;
  flex-direction: column;
  margin-left: 50px;
}

.contacts .phone {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  letter-spacing: 0.1em;
  color: #ffffff;
}

.contacts .region {
  font-size: 13px;
  text-align: right;
  letter-spacing: 0.1em;
  color: #444444;
  margin-top: 5px;
}

@media (max-width: 1500px) {
  .block:nth-child(2) {
    margin-left: 60px;
  }
}
@media (max-width: 1199.98px) {
  .block:nth-child(2) {
    margin-left: 10px;
  }
  ul li {
    margin: 0 10px;
  }
  .contacts {
    margin-left: 20px;
  }
}
@media (max-width: 991.98px) {
  .block:nth-child(2) {
    margin-left: 30px;
  }
  .nav-btn {
    display: block;
  }
  ul {
    position: fixed;
    background: #e00020;
    left: -100%;
    top: 0;
    width: 100%;
    height: 100%;
    flex-direction: column;
    justify-content: center;
    transition: 1s;
    opacity: 0;
  }
  ul.active {
    left: 0;
    opacity: 1;
  }
  ul li {
    margin: 20px;
  }
  ul li a {
    font-size: 20px;
  }
}
@media (max-width: 767.98px) {
  .contacts {
    display: none;
  }
}
@media (max-width: 575.98px) {
  .block:nth-child(3) {
    display: none;
  }
  .block:nth-child(2) {
    margin-left: auto;
  }
}
</style>
