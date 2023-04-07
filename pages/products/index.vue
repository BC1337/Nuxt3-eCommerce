<template>
    <div>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-5">
            <div v-for="product in products">
                <ProductCard :product="product"/>
            </div>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })

    // fetch the products
  const { data: products } =  await useFetch('https://fakestoreapi.com/products/')

    // overide the default head / meta content
    useHead({
        title: 'Nuxt Dojo | Merch',
        meta: [
            { name: 'description', content: 'Nuxt 3 Merch'}
        ]
    })

</script>

<style  scoped>

</style>