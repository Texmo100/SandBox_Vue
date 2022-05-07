<template>
  <div class="display">
    <Form
        v-model:first-name="firstName"
        v-model:last-name="lastName"
        v-model:gender="gender"
        v-model:favorite-food="favoriteFood"
    />
    <DataDisplay
      :firstName="firstName"
      :lastName="lastName"
      :gender="gender"
      :favoriteFood="favoriteFood"
    />
  </div>
</template>

<script>
import Form from "../../Form/Form.vue";
import DataDisplay from "../../DataDisplay/DataDisplay.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Display",
  components: {
    Form,
    DataDisplay,
  },
  data() {
    return {
      firstName: "",
      lastName: "",
      gender: "",
      favoriteFood: "",
    };
  }
};
</script>

<style scoped>
.display {
  width: 60%;
  height: 100%;
  background-color: rgba(0, 0, 0, 50%);
  display: flex;
  padding: 2rem;
  border-radius: 1rem;
}

@media screen and (max-width: 980px) {
  .display {
    width: 90%;
    flex-direction: column;
  }
}
</style>
