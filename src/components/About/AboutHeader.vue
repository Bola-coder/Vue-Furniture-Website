<template>
  <main>
    <div class="header">
      <h3>About <span>PlanckTops</span></h3>
    </div>
    <div class="content">
      <p>
        PlanckTops is a Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Quae, autem laudantium sit nemo nisi adipisci provident neque debitis et
        earum quis expedita mollitia quam culpa fugit aliquid optio quaerat sed
        facilis. Perspiciatis corporis voluptatum quasi aut, sed nemo animi vel
        nostrum nihil culpa pariatur voluptatem mollitia fugit aliquid magni rem
        architecto porro musdam aliquam laborum! Amet illo esse facilis quidem
        possimus sequi natus voluptate explicabo! Ea, tempora harum? Ea dicta
        molestias, minus corporis magnam consequatur necessitatibus laborum.
        Doloremque, repudiandae?
      </p>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");
main {
  margin-top: 8%;
  font-family: "Roboto", sans-serif;
  background: rgba(245, 240, 240, 0.8);
  padding: 20px;
}

.header {
  padding: 0px 20px;
}

.header h3 {
  width: 230px;
  font-size: 1.7rem;
  text-align: left;
  border-bottom: 3px solid rgb(189, 37, 37);
  margin-bottom: 20px;
}

span {
  color: rgb(189, 37, 37);
}

.content {
  padding: 20px 30px;
  width: 75%;
}

.content p {
  color: #000;
  text-align: left;
  letter-spacing: 1px;
  padding: 0 10px;
  border-left: 5px solid rgb(189, 37, 37);
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .content {
    width: 90%;
  }

  .content p {
    font-size: 20px;
  }
}

@media screen and (max-width: 425px) {
  .header h3 {
    width: 65vw;
    font-size: 2rem;
  }

  .content {
    padding: 10px 15px;
    width: 100%;
  }
  .content p {
    font-size: 25px;
  }
}
</style>
