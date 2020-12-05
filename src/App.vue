<template>
  <div id="app">
    <section-menu></section-menu>

    <page-footer></page-footer>
  </div>
</template>


<script>
import SectionMenu from "./components/SectionMenu.vue";
import PageFooter from "./components/PageFooter.vue";

export default {
  name: "App",
  components: {
    SectionMenu,
    PageFooter,
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

