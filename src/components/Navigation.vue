<template>
  <nav class="navBar">
    <h1 class="logo"><span>Abul</span>adze</h1>

    <ul v-show="!mobile" class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#skill">Skills</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="icon">
      <i
        @click="toggleMobileNav"
        v-show="mobile"
        class="fa-solid fa-bars"
        :class="{ 'icon-active': mobileNav }"
      ></i>
    </div>
    <transition name="mobile-nav">
      <ul v-show="mobileNav" class="dropdown-nav">
        <li><a @click="closeNavbar" href="#home">Home</a></li>
        <li><a @click="closeNavbar" href="#skill">Skills</a></li>
        <li><a @click="closeNavbar" href="#portfolio">Portfolio</a></li>
        <li><a @click="closeNavbar" href="#contact">Contact</a></li>
      </ul>
    </transition>
  </nav>
</template>

<script>
export default {
  name: "navigation",
  data() {
    return {
      mobile: null,
      mobileNav: false,
      windowWidth: null,
    };
  },

  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },

  methods: {

    closeNavbar(){
      this.mobileNav = false;
    },

    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      } else {
        this.mobile = false;
        this.mobileNav = false;
        return;
      }
    },
  },
};
</script>

<style>
.navBar {
  width: 100%;
  padding: 58px 61px 0px 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  z-index: 333;
}

.logo {
  font-weight: 400;
  font-size: 40px;
  line-height: 35px;
  color: #ffffff;
}

.logo span {
  font-weight: bold;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 76px;
}

.nav-links li {
  list-style-type: none;
}

.nav-links li a {
  text-decoration: none;
  font-weight: 400;
  font-size: 18px;
  line-height: 35px;
  color: rgba(255, 255, 255, 0.5);
  transition: all 0.5s;
}

.nav-links li a:hover {
  color: #ffffff;
}

.icon {
  display: flex;
  position: absolute;
  align-items: center;
  right: 30px;
  z-index: 999;
}

.icon .fa-bars {
  font-size: 25px;
  color: #ffff;
  cursor: pointer;
  transition: 0.5s ease all;
}

.fa-bars.icon-active {
  transform: rotate(180deg);
  color: black;
}

.dropdown-nav {
  display: flex;
  flex-direction: column;
  position: absolute;
  width: 100%;
  max-width: 250px;
  height: 100vh;
  background-color: #ffffff;
  top: 0;
  right: 0;
  padding-top: 70px;
  gap: 30px;
  z-index: 333;
}

.dropdown-nav li {
  list-style-type: none;
}

.dropdown-nav li a {
  text-decoration: none;
  color: #222222;
  font-size: 18px;
}

.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: all 0.5s ease;
}

.mobile-nav-enter-from,
.mobile-nav-enter-to {
  transform: translateX(250px);
}

.mobile-nav-enter-to {
  transform: translateX(0px);
}

@media (max-width: 900px) {
  .navBar {
    padding: 30px 30px 0px 30px;
  }

  .nav-links li a {
    font-size: 18px;
  }

  .logo {
    font-size: 28px;
  }
}
</style>
