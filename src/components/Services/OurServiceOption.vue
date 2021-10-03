<template>
  <main>
    <div class="service">
      <div class="left">
        <h2>{{ service.name }}</h2>
        <img :src="service.image" alt="" />
      </div>
      <div class="right">
        <p>{{ service.details }}</p>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  props: ["service"],
};
</script>

<style>
.service {
  width: 700px;
  padding: 20px 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  border-bottom: 2px solid rgb(189, 37, 37);
}

.right {
  flex-basis: 55%;
}

.service h2 {
  font-size: 1.7rem;
  padding: 5px;
  letter-spacing: 1px;
  color: rgb(189, 37, 37);
  margin-bottom: 10px;
}

.service img {
  width: 240px;
  height: 240px;
  border-radius: 30px;
}

.service p {
  padding: 20px;
  letter-spacing: 2px;
}

/* Responsivesness */

@media screen and (max-width: 768px) {
  .service {
    width: 650px;
    text-align: left;
  }

  .service h2 {
    font-size: 1.5rem;
  }

  .service p {
    font-size: 1.1rem;
  }
}
</style>
