<template>
  <div class="counter">
    <p :class=[indicatorClass]>{{ count }}</p>
    <span v-if="limitReachedDetector" class="limit-reached">Limit reached !</span>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Counter",
  props: ['count'],
  computed: {
    indicatorClass() {
      return this.count >= 10 ? 'indicator alert' : 'indicator'
    },
    limitReachedDetector() {
      return this.count >= 10 ? true : false;
    },
  },
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
  border-right: 1px solid #e8e8e8;
  display: flex;
  flex-direction: column;
}

@media screen and (max-width: 768px) {
  .counter {
    border: none;
    border-bottom: 1px solid #e8e8e8;
  }
}

.indicator {
  font-size: 5rem;
}

.alert {
  color: #E30B5C;
}

.limit-reached {
  color: #E30B5C;
}
</style>
