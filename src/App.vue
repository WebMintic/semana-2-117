<template>
  <div id="app">
    <page-footer></page-footer>
  </div>
</template>


<script>
import PageFooter from "./components/PageFooter.vue";

export default {
  name: "App",
  components: {
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

