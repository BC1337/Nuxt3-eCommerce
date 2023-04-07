<template>
    <!-- override default head behavior while using dynamic content -->
    <Head>
        <Title> Nuxt Dojo | {{ product.title }}</Title>
        <Meta name="description" :content:="product.description"></Meta>
    </Head>

    <!-- Display the product details component -->
    <div>
        <ProductDetails :product="product"/>
    </div>
</template>

<script setup>
    // descrutcture and extract the ID from the route params
    const { id } = useRoute().params

    // set uri to the dummy product data API + the specific product id
    const uri = 'https://fakestoreapi.com/products/' + id
    
    // fetch the product
    const { data: product } = await useFetch(uri, { key: id})

    // if no product is found, throw an error
    if (!product.value) {
        throw createError({ statusCode: 404, message: 'Product not found', fatal: true})
    }

    // apply custom nuxt layout to the product
    definePageMeta({
        layout: 'products'
    })
</script>

<style scoped>
    .thumb {
       max-height: 120px;
       max-width: 70%;
       margin: 0 auto; 
    }
</style>