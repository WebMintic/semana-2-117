<template>
  <div id="app">
    <section-menu></section-menu>
    <div class="container-fluid" id="news">
      <section-noticia></section-noticia>
    </div>
    <div class="container py-5 text-center" id="teams">
      <div class="row">
        <div class="col">
          <h1>Nuestro Equipo</h1>
          <p class="my-3">
            Nuestro equipo esta conformado por los mejores desarrolladores del
            programa MinTic2020, Son grandes trabajadores qeu aprenden muy
            rapido y trabajan muy bien en equipo
          </p>
        </div>
      </div>
      <div class="row justify-content-around">
        <team-card
          v-for="m in team"
          :key="m.codigo"
          v-bind:member="m"
        ></team-card>
      </div>
    </div>
    <page-footer></page-footer>
  </div>
</template>

<script>
import SectionMenu from "./components/SectionMenu.vue";
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue";
import SectionNoticia from "./components/SectionNoticia.vue";

export default {
  name: "App",
  components: {
    SectionMenu,
    PageFooter,
    TeamCard,
    SectionNoticia,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "Daniel Salazar",
          edad: 20,
          descripcion: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt 1",
          rol: "Development Team",
          image: "https://i.ibb.co/Gd4pPM3/danielsalazar.jpg",
        },
        {
          codigo: 2,
          nombre: "David Villa",
          edad: 30,
          descripcion: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt 1",
          rol: "Development Team",
          image: "https://i.ibb.co/P1C3yTZ/davidvilla.jpg",
        },
        {
          codigo: 3,
          nombre: "Ervid Molina",
          edad: 31,
          descripcion: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque quo vitae ut sunt 1",
          rol: "lead Team",
          image: "https://i.ibb.co/X35ZzPd/ervidmolina.jpg",
        },
      ],
    };
  },
};
</script>

