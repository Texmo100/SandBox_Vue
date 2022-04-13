<template>
  <div class="wrapper">
    <Display />
  </div>
</template>

<script>
import Display from "./components/Display/Display.vue";

export default {
  name: "App",
  components: {
    Display,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700&display=swap");

html {
  font-size: 62.5%;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

body {
  margin: 0;
  height: 100%;
  font-size: 1.6rem;
  font-family: "Open Sans", sans-serif;
}

p {
  margin: 0;
}
</style>

<style scoped>
.wrapper {
  height: 100vh;
  background-color: #2b2b2b;
  color: #e8e8e8;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}
</style>
