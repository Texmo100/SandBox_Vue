<template>
  <div class="card">
    <div class="card__image"></div>
    <div class="card__content">
      <p>{{title}}</p>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Card",
  props: {
    title: { type: String, required: true },
  }
};
</script>

<style scoped>
.card {
    background-color: #2b2b2b;
    color: #e8e8e8;
    display: flex;
    flex-direction: column;
    border-radius: 1rem;
    transition: all 200ms ease;
}

.card:hover {
  cursor: pointer;
  background-color: #333333;
  transform: scale(1.1);
}

.card__image, .card__content {
    flex: 1;
}

.card__image {
  width: 100%;
  height: 100%;
  background-image: url('../../assets/image_01.jpg');
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  border-radius: 1rem;
}

.card__content {
    display: flex;
    justify-content: center;
    border-radius: 1rem;
    padding: 1rem;
}

.card__content > p {
    font-size: 1.8rem;
    font-weight: 400;
}
</style>