<template>
  <div class="wrapper">
    <Title title="Image Gallery"/>
    <Gallery />
  </div>
</template>

<script>
import Gallery from './components/Gallery/Gallery.vue';
import Title from './components/Title/Title.vue';

export default {
  name: "App",
  components: {
    Gallery,
    Title,
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

p, h1 {
  margin: 0;
}
</style>

<style scoped>
.wrapper {
  min-height: 100vh;
  max-height: 100%;
  background-color: #e5e5e5;
  color: #2b2b2b;
  display: flex;
  justify-content: center;
  padding: 2rem;
}
</style>
