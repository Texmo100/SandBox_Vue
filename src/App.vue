<template>
  <div class="wrapper">
    <button type="button" class="btn" @click="showModal">Open Modal</button>
    <Modal v-show="isModalVisible" @close="closeModal" />
  </div>
</template>

<script>
import Modal from "./components/Modal/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
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
  background-color: #e8e8e8;
  color: #2b2b2b;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.btn {
  border: none;
  width: 10rem;
  height: 4rem;
  background-color: gray;
  color: aquamarine;
  border-radius: 1rem;
}

.btn:hover {
  cursor: pointer;
  background-color: #1f1f1f;
}
</style>
