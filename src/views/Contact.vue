<template>
  <div class="banner">
    <h2>Contact Us</h2>
  </div>
  <main>
    <div class="header">
      <h2>Send us a message</h2>
    </div>
    <form @submit.prevent="handleSubmit">
      <label>Name</label>
      <input type="text" required v-model="name" />
      <label>Email</label>
      <input type="email" required v-model="email" />
      <label>Message</label>
      <textarea v-model="message"></textarea>
      <div class="button    ">
        <button>Send Message</button>
      </div>
    </form>
  </main>
  <Footer />
</template>

<script>
import Footer from "../components/Footer.vue";
export default {
  components: { Footer },
  data() {
    return {
      name: "",
      email: "",
      message: "",
      data: {},
    };
  },

  methods: {
    handleSubmit() {
      this.data = { name: this.name, email: this.email, message: this.message };
      this.name = "";
      this.email = "";
      this.message = "";
      console.log(this.data);
    },
  },
};
</script>

<style scoped>
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

.header {
  text-align: center;
}
form {
  width: 700px;
  margin: 60px auto;
  padding: 5px;
  background: rgb(248, 245, 245);
  border-radius: 10px;
  border: none;
  box-shadow: 2px 2px 4px 2px rgb(126, 115, 115);
}

label {
  font-size: 12px;
  text-align: left;
  display: block;
  /* font-style: italic; */
  color: rgb(189, 37, 37);
  text-transform: uppercase;
  padding: 5px;
}

input,
textarea {
  padding: 10px;
  width: 90%;
  margin-left: 0;
  margin-right: auto;
  border-radius: 20px;
  border: none;
  box-shadow: 2px 2px 4px 2px rgb(126, 115, 115);
}
textarea {
  height: 170px;
  resize: none;
}

input:focus,
textarea:focus {
  outline: none;
}

.button {
  padding: 15px;
  text-align: right;
}

button {
  margin-top: 10px;
  /* display: block; */
  font-size: 1rem;
  padding: 10px 20px;
  border-radius: 15px;
  border: 0;
  color: #fff;
  background: rgb(189, 37, 37);
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .banner {
    height: 60vh;
  }

  .banner h2 {
    font-size: 4rem;
    left: 30%;
  }

  form {
    width: 650px;
    padding: 10px;
  }
  label {
    font-size: 15px;
    padding: 10px;
  }

  input,
  textarea {
    padding: 15px;
  }

  button {
    padding: 15px 20px;
    font-size: 1.2rem;
  }
}

@media screen and (max-width: 425px) {
  .banner {
    height: 70vh;
  }

  .banner h2 {
    font-size: 4.2rem;
    left: 14%;
  }

  form {
    width: 85vw;
  }
}
</style>
