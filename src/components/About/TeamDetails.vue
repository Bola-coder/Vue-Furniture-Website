<template>
  <main>
    <div class="container">
      <div class="teams" :class="checkId(team.id)">
        <div class="teams-main">
          <img :src="team.image" alt="" class="image" />
          <h3>{{ team.name }}</h3>
          <h5>{{ team.role }}</h5>
        </div>
        <div class="teams-sub">
          {{ team.details }}
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  props: ["team"],
  data() {
    return {
      className: null,
    };
  },
  methods: {
    checkId(id) {
      if (id % 2 == 0) {
        this.className = "right";
      } else {
        this.className = "left";
      }
      return this.className;
    },
  },
};
</script>

<style scoped>
main {
  padding: 10px;
}
.container {
  position: relative;
  padding: 10px 30px;
}

.container .left {
  margin-right: auto;
  margin-left: 0;
  border-left: 4px solid rgb(189, 37, 37);
  border-top: 10px solid rgb(189, 37, 37);
}
.container .right {
  margin-left: auto;
  margin-right: 0;
  border-right: 4px solid rgb(189, 37, 37);
  border-top: 10px solid rgb(189, 37, 37);
}
.teams {
  width: 700px;
  padding: 10px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  box-shadow: 2px 2px 9px 3px rgb(149, 155, 149);
}

.teams-main .image {
  width: 250px;
  height: 250px;
  border-radius: 30px;
}

.teams-main h3,
h5 {
  color: rgb(189, 37, 37);
}
h5 {
  font-style: italic;
  font-weight: lighter;
}

.teams-sub {
  width: 400px;
  font-size: 1.2rem;
  color: rgb(189, 37, 37);
  opacity: 0.8;
}

/* Responsiveness */

@media screen and (max-width: 768px) {
  .teams {
    width: 600px;
  }

  .teams-main .image {
    width: 220px;
    height: 220px;
  }

  .teams-sub {
    width: 350px;
  }
}

@media screen and (max-width: 425px) {
  .teams {
    padding: 20px;
    width: 80vw;
    flex-direction: column;
  }

  .teams-main h3 {
    margin-top: 20px;
    font-size: 1.5rem;
    margin-bottom: 10px;
  }

  .teams-sub {
    text-align: left;
    margin-top: 15px;
    width: 85%;
  }
}
@media screen and (max-width: 375px) {
  .teams {
    padding: 20px;
    width: 80vw;
    flex-direction: column;
  }

  .teams-main .image {
    width: 200px;
    height: 200px;
  }

  .teams-main h3 {
    margin-top: 20px;
    font-size: 1.3rem;
    margin-bottom: 10px;
  }

  .teams-sub {
    text-align: left;
    margin-top: 15px;
    width: 85%;
  }
}
</style>
