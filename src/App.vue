<template>
  <div class="wrapper">
    <Display />
  </div>
</template>

<script>
import Display from './components/UI/Display/Display.vue';

export default {
  name: "App",
  components: {
    Display,
  }
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
  background: rgb(2,0,36);
  background: linear-gradient(24deg, rgba(2,0,36,1) 0%, rgba(36,129,93,1) 52%, rgba(0,212,255,1) 100%);
  color: #e8e8e8;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}
</style>
