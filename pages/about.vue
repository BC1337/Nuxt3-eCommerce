<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, soluta quam ut deserunt at sequi veritatis illo quae unde molestias?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, soluta quam ut deserunt at sequi veritatis illo quae unde molestias?</p>
        <div>{{ data }}</div>
    </div>
</template>

<script setup>
    // feteching data from server as to not expose it to the user
    const { data } = await useFetch('/api/currency/GBP')
</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
p {
    margin: 20px 0;
}
</style>