<template>
  <main>
    <div class="banner">
      <h2>Our Services</h2>
    </div>
    <OurServices />
    <div class="call-to-action">
      <h4>Let us transform your home into an unrecognizable heaven</h4>
      <button>Contact us</button>
    </div>
  </main>
  <Footer />
</template>

<script>
import OurServices from "../components/Services/OurServices.vue";
import Footer from "../components/Footer.vue";
export default {
  components: { OurServices, Footer },
};
</script>

<style scoped>
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
  color: #fff;
  animation: moveInUp 1000ms ease-out;
}

.call-to-action {
  /* width: 900px;
  margin: 0 auto; */
  margin-top: 40px;
  padding: 30px;
  background: rgb(247, 241, 241);
}

.call-to-action h4 {
  font-size: 1.5rem;
  color: rgb(189, 37, 37);
  padding: 7px;
}

.call-to-action button {
  padding: 10px 17px;
  font-size: 1.4rem;
  border: none;
  border-radius: 10px;
  background: rgb(189, 37, 37);
  color: #fff;
  margin-top: 10px;
}

.call-to-action button:hover {
  background: rgb(236, 51, 51);
}

/* Animation */

@keyframes moveInUp {
  0% {
    opacity: 0;
    transform: translateY(120px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .banner {
    height: 60vh;
  }

  .banner h2 {
    font-size: 4rem;
    left: 27%;
  }
}
</style>
