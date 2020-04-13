<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import M from "materialize-css";

import Home from "./components/Home.vue";

export default {
  name: "App",

  mounted() {
    // initialize materialize.css
    M.AutoInit();
  },
  components: {
    Home
  }
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
