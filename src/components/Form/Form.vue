<template>
  <form>
    <p>Form</p>
    <div class="form-item">
      <label class="form-item__label">First Name</label>
      <input
        class="form-item__input"
        :value="firstName"
        @input="$emit('update:firstName', $event.target.value)"
        placeholder="first name"
      />
    </div>

    <div class="form-item">
      <label class="form-item__label">Last Name</label>
      <input
        class="form-item__input"
        :value="lastName"
        @input="$emit('update:lastName', $event.target.value)"
        placeholder="last name"
      />
    </div>

    <div class="form-item">
      <label class="form-item__label">Gender</label>
      <div class="radio-item">
        <input
          class="radio-item__input"
          type="radio"
          value="male"
          :checked="gender == 'male'"
          @change="$emit('update:gender', $event.target.value)"
        />
        <label class="radio-item__label">male</label>
      </div>

      <div class="radio-item">
        <input
          class="radio-item__input"
          type="radio"
          value="female"
          :checked="gender == 'female'"
          @change="$emit('update:gender', $event.target.value)"
        />
        <label class="radio-item__label">female</label>
      </div>
    </div>

    <div class="form-item">
        <label class="form-item__label">Favorite food</label>
        <select  class="select-item" @change="$emit('update:favoriteFood', $event.target.value)">
            <option class="select-item__option" value="" hidden>Please select one</option>
            <option class="select-item__option" value="sushi">Sushi</option>
            <option class="select-item__option" value="pizza">Pizza</option>
            <option class="select-item__option" value="hamburguer">Hamburguer</option>
        </select>
    </div>
  </form>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Form",
  props: {
    firstName: String,
    lastName: String,
    gender: String,
    favoriteFood: String,
  },
};
</script>

<style scoped>
form {
  flex: 1;
  display: flex;
  flex-direction: column;
  border-right: 1px solid #e8e8e8;
}

@media screen and (max-width: 980px) {
  form {
    border: none;
  }
}

form > p {
  align-self: center;
  font-size: 3rem;
}

.form-item {
  display: flex;
  flex-direction: column;
  margin: 1rem;
}

.form-item__label {
  font-size: 1.8rem;
  margin-bottom: 0.5rem;
}

.form-item__input {
  display: block;
  border: none;
  width: 100%;
  height: 4rem;
  background-color: rgba(255, 255, 255, 25%);
  border-radius: 1rem;
  padding: 0.5rem;
  color: white;
  font-size: 1.6rem;
}

.form-item__input::placeholder {
  color: #c1c1c1;
}

.radio-item {
  display: flex;
  align-items: center;
  margin: 0.5rem 0;
}

.radio-item__input {
  width: 2rem;
  height: 2rem;
  margin: 0;
  margin-right: 0.5rem;
}

.select-item {
    width: 100%;
    height: 4rem;
    padding: 0.5rem;
    background-color: rgba(255, 255, 255, 25%);
    border-radius: 1rem;
    color: #e8e8e8;
}

.select-item__option {
    color: #2b2b2b;
}
</style>
