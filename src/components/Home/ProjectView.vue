<template>
  <div class="project">
    <img :src="project.image" class="project-image" />
    <div class="text">
      <h2 class="project-name">{{ project.name }}</h2>
      <p class="project-detail">{{ project.detail }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["project"],
};
</script>

<style scoped>
.project {
  max-width: 300px;
  /* padding: 20px 5px; */
  /* border: 3px solid black; */
  box-shadow: 4px 4px 5px rgba(44, 40, 40, 0.2);
}
.project:hover {
  border-bottom: 4px solid rgb(189, 37, 37);
}
.project-image {
  width: 300px;
  height: 250px;
}

.text {
  padding: 20px;
  text-align: center;
}

.project-name {
  text-align: left;
  font-size: 20px;
  color: #222;
  margin-bottom: 5px;
  color: rgb(189, 37, 37);
}

.project-detail {
  letter-spacing: 3px;
  font-size: 12px;
  color: #000;
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .project-name {
    font-size: 25px;
  }
  .project-detail {
    font-size: 15px;
  }
}

@media screen and (max-width: 425px) {
  .text {
    padding: 15px;
  }
}

@media screen and (max-width: 375px) {
  .project {
    max-width: 280px;
  }
}
@media screen and (max-width: 425px) {
}
</style>
