<template>
  <div>
    <app-header></app-header>

    <div class="container">
      <div class="row">
        <div class=".center-align col-8">
          <app-todos></app-todos>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./shared/Header";
import Todos from "./Todos";

export default {
  components: {
    "app-header": Header,
    "app-todos": Todos
  },

  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
