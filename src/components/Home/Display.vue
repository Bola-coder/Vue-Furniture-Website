<template>
  <div class="display">
    <div class="display-text">
      <p>
        Do you need a very competent and reliable team to help transform your
        home to a paradise on earth?, Our team of experienced designers is the
        right plug for you. Let us perform wonders on your home
      </p>
      <button>Contact Us</button>
    </div>
    <div class="display-image">
      <img :src="image" alt="bed-image" />
    </div>
  </div>
</template>

<script>
import bed from "../../assets/bedOne.jpg";
export default {
  data() {
    return {
      image: bed,
    };
  },
};
</script>

<style scoped>
.display {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px;
  margin-top: 120px;
  background: linear-gradient(rgb(114, 110, 110), rgb(66, 65, 65));
}

.display-text {
  width: 70%;
  text-align: left;
}
.display-text p {
  font-size: 1.5rem;
  line-height: 2.5rem;
  color: rgb(248, 242, 242);
}
.display-text button {
  padding: 8px 16px;
  font-size: 1.3rem;
  color: #fff;
  background: rgb(189, 37, 37);
  border: none;
  border-radius: 12px;
  margin-top: 30px;
  letter-spacing: 2px;
  cursor: pointer;
}

.display-text button:hover {
  /* opacity: 0.8; */
  background: #fff;
  color: rgb(189, 37, 37);
}

.display-image {
  flex-basis: 50%;
}

.display-image img {
  width: 400px;
  height: 400px;
  border-radius: 50%;
  box-shadow: 2px 1px 2px 4px rgb(199, 207, 199),
    1px 2px 2px 3px rgb(218, 228, 218);
}

/* Resposiveness */
@media screen and (max-width: 768px) {
  .display {
    padding: 20px;
  }

  .display-text p {
    font-size: 1.3rem;
  }
  .display-image img {
    width: 320px;
    height: 320px;
  }
}
</style>
