<template>
  <div class="nav">
    <div class="logo">
      PlanckTops
    </div>
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="">Services</router-link>
      <router-link to="">Contact</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  component: {},
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
  /* transform: rotate(4px, 9px); */
}
</style>
