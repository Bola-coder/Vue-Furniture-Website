<template>
  <img
    :src="src"
    alt="Hamburger menu for smaller
        devices"
    @click="
      handleToggle();
      handleClick();
    "
  />
</template>

<script>
import one from "../assets/hamburger.png";
import two from "../assets/hamcancel.png";

export default {
  data() {
    return {
      active: false,
      src: one,
    };
  },
  methods: {
    handleToggle() {
      this.active = !this.active;
      this.$emit("clicked", this.active);
    },
    handleClick() {
      this.active ? (this.src = two) : (this.src = one);
    },
  },
};
</script>

<style>
img {
  width: 60px;
}

@media screen and (max-width: 425px) {
  img {
    width: 45px;
  }
}
</style>
