<template>
  <div class="display">
    <Counter :count="count" />
    <Actions :increment="increment" :decrement="decrement" />
  </div>
</template>

<script>
import Counter from "../Counter/Counter.vue";
import Actions from "../Actions/Actions.vue";

const counterHandler = (counter, limit, action) => {
  if (action === "increment") {
    const counterIncremented = counter + 1;
    return counter >= limit ? counter : counterIncremented;
  } else if (action === "decrement") {
    const counterDecremented = counter - 1;
    return counter <= limit ? counter : counterDecremented;
  }
};

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Display",
  components: {
    Counter,
    Actions,
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count = counterHandler(this.count, 10, "increment");
    },
    decrement() {
      this.count = counterHandler(this.count, 0, "decrement");
    },
  },
};
</script>

<style scoped>
.display {
  width: 50%;
  height: 50%;
  background-color: #212121;
  border-radius: 1rem;
  display: flex;
}

@media screen and (max-width: 768px) {
  .display {
    flex-direction: column;
  }
}
</style>
