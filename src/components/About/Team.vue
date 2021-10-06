<template>
  <main>
    <div class="header">
      <h3>Our <span>Team</span></h3>
    </div>
    <div class="details" v-for="team in teams" :key="team.id">
      <TeamDetails :team="team" />
    </div>
  </main>
</template>

<script>
import TeamDetails from "./TeamDetails.vue";
import man1 from "../../assets/man1.jpg";
import guy from "../../assets/guy.jpg";

export default {
  components: { TeamDetails },
  data() {
    return {
      teams: [
        {
          id: 1,
          name: "Mr John Park",
          image: man1,
          role: "Chief Executive Officer",
          details:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus eligendi qiat repellendus ipsa molestias odio sapiente dolorum error aperiam laborum sequi? Fugit amet libero eius quo illum enim et veniam sed?",
        },
        {
          id: 2,
          name: "Mrs Allen Judith",
          image: guy,
          role: "Customer Care Lead",
          details:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus eligendi quis modi recusandae voluptatum maxime, odio nesciunt, veritatis vel quisquam molestiae debitis quas! Ipsum dolores deled?",
        },
        {
          id: 3,
          name: "Grant Fishergul",
          image: man1,
          role: "Lead Technical Officer",
          details:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus eligendi quis modi recusandae voluptatum maxime, odio nesciunt, veritatis vel quisquam molestiae debitis quas! Ipsum dolores deleniti t fugid?",
        },
      ],
    };
  },
};
</script>

<style scoped>
.header {
  margin-top: 7%;
}
.header h3 {
  font-size: 2.2rem;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.header h3 span {
  color: rgba(189, 37, 37, 0.9);
}

/* Responsiveness */
@media screen and (max-width: 768px) {
  .header {
    margin-top: 10%;
  }
}

@media screen and (max-width: 425px) {
  .header h3 {
    font-size: 2.4rem;
  }
}

@media screen and (max-width: 375px) {
  .header h3 {
    font-size: 2.2rem;
  }
}
</style>
