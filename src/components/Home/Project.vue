<template>
  <div class="block">
    <h3>Good furnitures brings out the real beauty of your homes</h3>
    <div class="project-block">
      <div class="projects" v-for="project in projects" :key="project.name">
        <ProjectView :project="project" />
      </div>
    </div>
  </div>
</template>

<script>
import ProjectView from "./ProjectView.vue";
import one from "../../assets/decor1.jpg";
import two from "../../assets/decor2.jpg";
import three from "../../assets/decor3.jpg";
import four from "../../assets/decor4.jpg";
import five from "../../assets/decor5.jpg";

export default {
  components: { ProjectView },
  data() {
    return {
      projects: [
        {
          name: "One and beauty",
          detail:
            " Lorem ipsum dolor sit amet consectta earum itaque fuga error delectus aspernatur temporibus eius?",
          image: one,
        },
        // {
        //   name: "Two and beauty",
        //   detail:
        //     " Lorem ipsum dolor sit amet consectta earum itaque fuga error delectus aspernatur temporibus eius?",
        //   image: two,
        // },
        // {
        //   name: "Three and beauty",
        //   detail:
        //     " Lorem ipsum dolor sit amet consectta earum itaque fuga error delectus aspernatur temporibus eius?",
        //   image: three,
        // },
        {
          name: "Four and beauty",
          detail:
            " Lorem ipsum dolor sit amet consectta earum itaque fuga error delectus aspernatur temporibus eius?",
          image: four,
        },
        {
          name: "Five and beauty",
          detail:
            " Lorem ipsum dolor sit amet consectta earum itaque fuga error delectus aspernatur temporibus eius?",
          image: five,
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.block {
  margin-top: 120px;
  /* padding: 10px; */
}

.block h3 {
  font-size: 2rem;
}
.project-block {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 40px;
}
.projects {
  padding: 20px;
  clip-path: polygon(10% 0, 90% 0, 100% 100%, 0% 100%);
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .block {
    margin-top: 90px;
    padding: 5px;
  }

  .block h3 {
    font-size: 1.8rem;
  }

  .projects {
    padding: 15px;
  }
}
</style>
