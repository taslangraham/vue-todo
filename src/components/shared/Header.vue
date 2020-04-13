<template>
  <div>
    <nav class="teal lighten-2">
      <div class="nav-wrapper">
        <a href="/" class="brand-logo center">{{navTitle}}</a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navTitle: "Todist"
    };
  }
};
</script>