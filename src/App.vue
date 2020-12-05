<template>
  <div id="app">
    <section-menu></section-menu>
    <div class="container-fluid">
      <section-noticia></section-noticia>
    </div>
    <page-footer></page-footer>
  </div>
</template>


<script>
import SectionMenu from "./components/SectionMenu.vue";
import PageFooter from "./components/PageFooter.vue";
import SectionNoticia from "./components/SectionNoticia.vue";

export default {
  name: "App",
  components: {
    SectionMenu,
    PageFooter,
    SectionNoticia,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "",
          descrpcion: "",
          rol: "",
          image: "",
        },
      ],
    };
  },
};
</script>

