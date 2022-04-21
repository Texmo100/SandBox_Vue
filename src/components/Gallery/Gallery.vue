<template>
  <div class="gallery">
    <Card v-for="item in items" :key="item.id" :title="item.title" />
  </div>
</template>

<script>
import Card from "../Card/Card.vue";

const itemGenerator = number => {
  const dummyArray = [];

  for(let i = 0; i < number; i++){
      let item = { id: i, title: `card_${i}`};
      dummyArray.push(item);
  }

  return dummyArray;
};

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Gallery",
  components: {
    Card,
  },
  data() {
    return {
      items: itemGenerator(16),
    };
  },
};
</script>

<style scoped>
.gallery {
  margin-top: 8rem;
  width: 80%;
  height: 100%;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(25rem, 1fr);
  gap: 2rem;
}

@media screen and (max-width: 1000px) {
  .gallery {
    grid-template-columns: 1fr;
    grid-template-columns: repeat(2, 1fr);
  }
}

@media screen and (max-width: 768px) {
  .gallery {
    grid-template-columns: 1fr;
  }
}
</style>