<template>
  <img
    src="../assets/hamburger.png"
    alt="Hamburger menu for smaller
        devices"
    @click="handleToggle"
  />
</template>

<script>
export default {
  data() {
    return {
      active: false,
    };
  },
  methods: {
    handleToggle() {
      this.active = !this.active;
      this.$emit("clicked", this.active);
    },
  },
};
</script>

<style>
img {
  width: 60px;
}
</style>
