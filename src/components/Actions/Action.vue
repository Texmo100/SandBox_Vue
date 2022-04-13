<template>
  <div class="action">
    <p>{{ label }}</p>
    <button @click="functionAction()">{{ value }}</button>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Action",
  props: ["label", "value", "functionAction"],
};
</script>

<style scoped>
.action {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.action button {
  width: 8rem;
  height: 8rem;
  display: block;
  border: none;
  margin: 1rem;
  padding: 0.5rem;
  background-color: #333333;
  color: #e8e8e8;
  border-radius: 1rem;
  transition: all 200ms ease;
  font-size: 1.8rem;
}

.action button:hover {
  cursor: pointer;
  transform: scale(1.1);
  color: #2b2b2b;
  background-color: #e8e8e8;
}

.action button:active {
  transform: scale(1.2);
  background-color: aquamarine;
}
</style>