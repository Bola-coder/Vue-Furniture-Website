<template>
  <div class="nav">
    <div class="logo" @click="handleLogoClick">
      PlanckTops
    </div>

    <nav>
      <div class="desktop">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/service">Services</router-link>
        <router-link to="/contact">Contact</router-link>
      </div>
      <div class="mobile">
        <Hamburger @clicked="handleClicked" />
      </div>
    </nav>
  </div>
</template>

<script>
import Hamburger from "./Hamburger.vue";
export default {
  name: "NavBar",
  components: { Hamburger },
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    handleLogoClick() {
      this.$router.push({ name: "Home" });
    },
    handleClicked(active) {
      active ? (this.showMenu = true) : (this.showMenu = false);
      this.$emit("hamClick", this.showMenu);
    },
  },
};
</script>

<style scoped>
.nav {
  max-width: 100vw;
  max-height: 15vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  position: sticky;
  top: 0;
  z-index: 10;
  background: #fff;
  box-shadow: 0 1px 1px rgb(82, 72, 72);
}

.logo {
  font-size: 2rem;
  font-weight: bolder;
  color: rgb(189, 37, 37);
  cursor: pointer;
}

nav {
  margin-right: 20px;
}

.mobile {
  display: none;
}

nav a {
  padding: 4px 20px;
  text-decoration: none;
  font-size: 1.1rem;
  font-weight: bold;
  color: rgb(199, 56, 56);
  /* transition: width 2s ease-out; */
}

nav a:hover {
  background: rgb(187, 51, 78);
  border-radius: 15px;
  color: #fff;
  /* text-decoration: underline;
  transform: translateY(-5%); */
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .logo {
    margin-left: 20px;
  }
  .desktop {
    display: none;
  }

  .mobile {
    display: block;
    padding: 5px;
  }

  /* .mobile img {
    width: 60px;
  } */
}

@media screen and (max-width: 375px) {
  .logo {
    margin-left: 10px;
    font-size: 1.7rem;
  }
  .mobile {
    padding: 0;
  }
}
</style>
