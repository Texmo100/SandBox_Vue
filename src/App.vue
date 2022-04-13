<template>
  <div class="wrapper">
    <div class="display">
      <div class="counter">
        {{count}}
      </div>
      <div class="actions">
        <div class="action">
          <p>Increment</p>
          <button @click="increment()">+</button>
        </div>
        
        <div class="action">
          <p>Decrement</p>
          <button @click="decrement()">-</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const counterHandler = (counter, limit, action) => {
  if(action === 'increment'){
    const counterIncremented = counter + 1;
    return counter >= limit ? counter : counterIncremented;
  }else if(action === 'decrement'){
    const counterDecremented = counter - 1;
    return counter <= limit ? counter : counterDecremented;
  }
};

export default {
  name: "App",
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count = counterHandler(this.count, 10, 'increment');
    },
    decrement() {
      this.count = counterHandler(this.count, 0, 'decrement');
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
  background-color: #2b2b2b;
  color: #e8e8e8;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.display {
  width: 50%;
  height: 50%;
  background-color: #212121;
  border-radius: 1rem;
  display: flex;
}

@media screen and (max-width: 768px){
  .display {
    flex-direction: column;
  }
}

.counter, .actions {
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

.actions {
  justify-content: center;
  align-items: center;
}

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
