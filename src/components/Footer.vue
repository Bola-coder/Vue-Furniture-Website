<template>
  <footer>
    <div class="footer-content">
      <div class="footer-links">
        <p>Quick Links</p>
        <router-link to="/">Home</router-link> <br />
        <router-link to="/about">About</router-link> <br />
        <router-link to="/service">Service</router-link> <br />
        <router-link to="/contact">Contact</router-link> <br />
      </div>
      <div class="footer-media">
        <p>Socials</p>
        <a href="#" target="_blank">Twitter</a> <br />
        <a href="#" target="_blank">Instagram</a> <br />
        <a href="#" target="_blank">Facebook</a> <br />
      </div>
    </div>
    <p>&copy; Abatoms technologies 2021 all right reserved</p>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
footer {
  margin-top: 10%;
  padding: 10px;
  background: linear-gradient(rgb(129, 126, 126), rgb(71, 68, 68));
}
.footer-content {
  width: 700px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  /* padding: 10px; */
}

.footer-links,
.footer-media {
  padding: 10px;
}
.footer-links p,
.footer-media p {
  padding: 10px;
  font-size: 1.3rem;
}
.footer-links a,
.footer-media a {
  font-size: 1rem;
  /* padding: 20px; */
  text-decoration: none;
  color: #ddd;
}
a:hover {
  text-decoration: underline;
}
p {
  color: #fff;
}

/* Responsiveness */
@media screen and (max-width: 425px) {
  .footer-content {
    width: 90vw;
    justify-content: space-between;
  }

  .footer-links,
  .footer-media {
    padding: 20px;
  }

  .footer-links a,
  .footer-media a {
    font-size: 1.2rem;
  }
}

@media screen and (max-width: 375px) {
  .footer-links,
  .footer-media {
    padding: 10px;
  }
}
</style>
