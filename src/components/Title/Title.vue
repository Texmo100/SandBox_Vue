<template>
  <div class="header">
    <h1 class="title">{{title}}</h1>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Title",
  props: {
      title: { type: String, required: true },
  }
};
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  width: 80%;
  height: 6rem;
  background-color: rgba(0, 0, 0, 50%);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #e8e8e8;
  border-bottom-left-radius: 1rem;
  border-bottom-right-radius: 1rem;
  z-index: 3;
}

.title {
  font-size: 2.2rem;
  font-weight: 700;
}
</style>