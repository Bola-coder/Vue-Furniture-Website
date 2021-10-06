<template>
  <main>
    <div class="header">
      <h2>What we do</h2>
    </div>
    <div class="content" v-for="service in services" :key="service.id">
      <OurServiceOption :service="service" />
    </div>
  </main>
</template>

<script>
import OurServiceOption from "./OurServiceOption.vue";
import bedOne from "../../assets/bedOne.jpg";
import decor1 from "../../assets/decor1.jpg";
import decor2 from "../../assets/decor2.jpg";
import decor3 from "../../assets/decor3.jpg";

export default {
  components: { OurServiceOption },
  data() {
    return {
      services: [
        {
          id: 1,
          name: "Furniture Making",
          image: bedOne,
          details:
            " Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magni cumque natus qui quaerat. Nam unde dolores, ratione incidunt id doloremque? Possimus illum nostrum expedita incidunt officia fugiat excepturi delectus dolorem, pariatur nesciunt repudiandae et velit officiis doloremque corporis debitis.",
        },
        {
          id: 2,
          name: "Interior decoration",
          image: decor1,
          details:
            " Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magni cumque natus qui quaerat. Nam unde dolores, ratione incidunt id doloremque? Possimus illum nostrum expedita incidunt officia fugiat excepturi delectus dolorem, pariatur nesciunt repudiandae et velit officiis doloremque corporis debitis.",
        },
        {
          id: 3,
          name: "Furniture Repair ",
          image: decor2,
          details:
            " Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magni cumque natus qui quaerat. Nam unde dolores, ratione incidunt id doloremque? Possimus illum nostrum expedita incidunt officia fugiat excepturi delectus dolorem, pariatur nesciunt repudiandae et velit officiis doloremque corporis debitis.",
        },
        {
          id: 4,
          name: "Buying Furnitures",
          image: decor3,
          details:
            " Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magni cumque natus qui quaerat. Nam unde dolores, ratione incidunt id doloremque? Possimus illum nostrum expedita incidunt officia fugiat excepturi delectus dolorem, pariatur nesciunt repudiandae et velit officiis doloremque corporis debitis.",
        },
      ],
    };
  },
};
</script>

<style>
main {
  padding: 20px;
}

.header {
  margin-top: 7%;
}
.header h2 {
  font-size: 2rem;
  color: rgb(189, 37, 37);
  font-style: oblique;
}

/* Responsiveness */
@media screen and (max-width: 768px) {
  .header {
    margin-top: 10%;
  }

  .header h2 {
    font-size: 2.2rem;
  }
}

@media screen and (max-width: 425px) {
  .header h2 {
    font-size: 2.4rem;
  }
}
</style>
