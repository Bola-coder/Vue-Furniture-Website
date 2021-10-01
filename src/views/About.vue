<template>
  <main>
    <div class="banner">
      <h2>About Us</h2>
    </div>
    <AboutHeader />
    <Team />
    <Footer />
  </main>
</template>

<script>
import AboutHeader from "../components/About/AboutHeader.vue";
import Team from "../components/About/Team.vue";
import Footer from "../components/Footer";

export default {
  components: { AboutHeader, Team, Footer },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.banner {
  max-width: 100vw;
  height: 65vh;
  background: url("../assets/carpenter.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.banner h2 {
  text-align: center;
  font-size: 4.5rem;
  text-transform: uppercase;
  font-family: "Roboto", sans-serif;
  position: absolute;
  left: 35%;
  top: 40%;
  /* transform: translate(-5%, -10%); */
  color: #fff;
  animation: moveInUp 1000ms ease-out;
}

@keyframes moveInUp {
  0% {
    opacity: 0;
    transform: translateY(-120px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
