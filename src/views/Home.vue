<template>
  <div class="home">
    <div class="heroSection">
      <div class="hero-text">
        <h1>Beautifying homes</h1>
        <p>Need an excellent design? We work to satisfy our customers</p>
        <button>Request our service</button>
      </div>
    </div>
  </div>
  <Project />
  <Display />
  <Footer />
</template>

<script>
import Project from "../components/Home/Project";
import Display from "../components/Home/Display";
import Footer from "../components/Footer";

export default {
  name: "Home",
  components: { Project, Display, Footer },
};
</script>

<style scoped>
.home {
  max-width: 100vw;
  height: 92vh;
  background-image: linear-gradient(
      to right bottom,
      rgba(68, 75, 67, 0.8),
      rgba(39, 51, 47, 0.8)
    ),
    url("../assets/carpenter.jpg");

  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.heroSection {
  position: absolute;
  top: 20%;
  right: 30%;
  /* width: 60%; */
}

.hero-text {
  transform: translate(20%, 40%);
}
.hero-text h1 {
  color: #fff;
  font-size: 3.7rem;
  text-transform: uppercase;
  animation: moveInLeft 2s ease-out;
}

.hero-text p {
  color: #fff;
  font-size: 1.2rem;
  font-weight: bold;
  letter-spacing: 3px;
  animation: moveInRight 2s ease-out;
  margin-top: 15px;
}

button {
  padding: 10px 12px;
  margin-top: 30px;
  background: rgb(197, 44, 44);
  color: #fff;
  border: none;
  border-radius: 20px;
  text-transform: uppercase;
  animation: buttonMove 2s ease-out;
  transition: all 0.5s;
  cursor: pointer;
}
button:hover {
  transform: translateY(-2px);
  opacity: 0.7;
}

@keyframes moveInLeft {
  0% {
    opacity: 0;
    transform: translateX(-5rem);
  }
  80% {
    transform: translateX(1rem);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
@keyframes moveInRight {
  0% {
    opacity: 0;
    transform: translateX(5rem);
  }
  80% {
    transform: translateX(-1rem);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes buttonMove {
  0% {
    opacity: 0;
    transform: translateY(5rem);
  }
  80% {
    transform: translateY(-1rem);
  }
  100% {
    transform: translateY(0);
  }
}

/* Responsiveness */
@media screen and (max-width: 768px) {
  .home {
    height: 75vh;
  }

  .hero-text h1 {
    font-size: 3rem;
  }

  .hero-text p {
    font-size: 1.2rem;
  }
  button {
    font-size: 20px;
    margin-top: 25px;
  }
}

@media screen and (max-width: 425px) {
  .heroSection {
    top: 10%;
  }
  .hero-text h1 {
    font-size: 3rem;
  }

  .hero-text p {
    font-size: 1.1rem;
  }

  button {
    font-size: 18px;
    padding: 12px 15px;
  }
}
@media screen and (max-width: 375px) {
  /* .home {
    height: 65vh;
  } */
  .hero-text h1 {
    font-size: 2.6rem;
  }
  button {
    font-size: 15px;
    padding: 12px 14px;
  }
}
@media screen and (max-width: 320px) {
  .hero-text h1 {
    font-size: 2.2rem;
  }
}
</style>
