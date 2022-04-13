<template>
  <div class="actions">
    <Action label="Increment" value="+" :functionAction="increment" />
    <Action label="Decrement" value="-" :functionAction="decrement" />
  </div>
</template>

<script>
import Action from "./Action.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Actions",
  props: ["increment", "decrement"],
  components: {
    Action,
  },
};
</script>

<style scoped>
.actions {
  flex: 1;
  display: flex;
}

.actions {
  justify-content: center;
  align-items: center;
}
</style>