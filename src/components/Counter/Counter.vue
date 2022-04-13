<template>
  <div class="counter">
    {{ count }}
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Counter",
  props: ['count'],
};
</script>

<style scoped>
.counter {
  flex: 1;
  display: flex;
}

.counter {
  justify-content: center;
  align-items: center;
  font-size: 4rem;
  border-right: 1px solid #e8e8e8;
}

@media screen and (max-width: 768px) {
  .counter {
    border: none;
    border-bottom: 1px solid #e8e8e8;
  }
}
</style>
