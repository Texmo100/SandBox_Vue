<template>
    <div class="data-display">
        <p>Data</p>
        <span class="data-item">First name: {{ firstName }}</span>
        <span class="data-item">Last name: {{ lastName }}</span>
        <span class="data-item">Gender: {{ gender }}</span>
        <span class="data-item">Favorite food: {{ favoriteFood }}</span>
    </div>
</template>

<script>
export default {
    name: 'DataDisplay',
    props: {
        firstName: String,
        lastName: String,
        gender: String,
        favoriteFood: String,
    }
}
</script>

<style scoped>
.data-display {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.data-display > p {
    font-size: 3rem;
    margin-bottom: 2rem;
}

.data-item {
    margin: 2rem 0;
}
</style>
