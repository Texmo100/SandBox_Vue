<template>
  <div class="wrapper">
    <p>Hey this is the SandBox Vue</p>
  </div>
</template>

<script>
export default {
  name: "App",
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
