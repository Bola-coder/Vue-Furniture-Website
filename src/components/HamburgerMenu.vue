<template>
  <div class="nav">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/service">Services</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.nav {
  display: block;
  position: fixed;
  width: 200px;
  top: 10vh;
  right: 0;
  z-index: 200;
  background: #fff;
}
nav {
  top: 20px;
  padding: 15px;
  /* background: rgb(189, 37, 37); */
  animation: hamburger 1.5s ease-out;
}

nav a {
  display: block;
  padding: 20px;
  font-size: 2rem;
  text-align: left;
  text-decoration: none;
  color: rgb(189, 37, 37);
  /* font-weight: bold; */
}
nav a:hover {
  text-decoration: underline;
}

@keyframes hamburger {
  0% {
    opacity: 0.7;
  }

  100% {
    opacity: 1;
  }
}

@media screen and (max-width: 425px) {
  nav {
    padding: 12px;
  }

  nav a {
    padding: 8px;
  }
}
</style>
