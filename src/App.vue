<template>
  <div id="app">
    <div class="container my-5 py-5 text-center">
      <div class="row mb-5">
          <div class="col">
              <h1>Nuestro Equipo</h1>
              <p class="my-3">Nuestro equipo esta conformado por los mejores desarrolladores del programa MinTic2020, Son grandes 
                trabajadores qeu aprenden muy rapido y trabajan muy bien en equipo
              </p>
          </div>
      </div>
      <div class="row justify-content-around">
        <team-card v-for="m in team" :key="m.codigo" v-bind:member="m"></team-card>
      </div>
    </div>
    <page-footer></page-footer>
  </div>
</template>


<script>
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue"

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
  },
  data() {
    return {
      team: [
        {
            codigo: 1,
            nombre: 'Daniel Salazar',
            edad: 20,
            descripcion:{
              ocupacion: 'Estudiante de Ingeniería Multimedia.',
              residencia: 'Chía, Cundinamarca.',
              pasatiempos: 'Jugar baloncesto, salir de fiesta, hacer caminata',
              } ,
            rol: 'Development Team',
            image: 'https://i.ibb.co/Gd4pPM3/danielsalazar.jpg'
        },
        {
            codigo: 2,
            nombre: 'David Villa',
            edad: 30,
            descripcion: {
              ocupacion: 'Ingeniero mecánico - Desarrollador móvil',
              residencia: 'Bogotá, Cundinamarca',
              pasatiempos: 'Jugar fútbol, voleibol, bailar',
            },
            rol: 'Development Team',
            image: 'https://i.ibb.co/P1C3yTZ/davidvilla.jpg'
        },
        {
            codigo: 3,
            nombre: 'Ervid Molina',
            edad: 31,
            descripcion: {
              ocupacion: 'Ingeniero de Control - Desarrollador de videojuegos.',
              residencia: 'Medellín, Antioquia.',
              pasatiempos: 'Ver y jugar fútbol, ver Fórmula 1, series y películas, jugar videojuegos.',
            },
            rol: 'lead Team',
            image: 'https://i.ibb.co/X35ZzPd/ervidmolina.jpg'
        }
      ],
    };
  },
};
</script>

