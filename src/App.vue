<template>
  <NavBar @hamClick="displayMobileMenu" />
  <div class="hamburger-menu" v-if="displayMenu">
    <HamburgerMenu />
  </div>
  <router-view />
</template>

<script>
import NavBar from "./components/NavBar.vue";
import HamburgerMenu from "./components/HamburgerMenu.vue";

export default {
  components: { NavBar, HamburgerMenu },
  data() {
    return {
      displayMenu: false,
    };
  },
  methods: {
    displayMobileMenu(value) {
      value ? (this.displayMenu = true) : (this.displayMenu = false);
    },
  },
};
</script>
<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1d1919;
}
</style>
