<template>
    <div>
        <h2>Home</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, soluta quam ut deserunt at sequi veritatis illo quae unde molestias?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, soluta quam ut deserunt at sequi veritatis illo quae unde molestias?</p>
    </div>
</template>

<script setup>

</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
p {
    margin: 20px 0;
}

.grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1rem;
    }
</style>