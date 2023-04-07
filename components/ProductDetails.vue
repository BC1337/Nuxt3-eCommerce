<template>
    <div class="card">
      <div class="grid gap-10 md:grid-cols-2 md:flex-col">
        <div class="p-7">
          <img :src="product.image" alt="product image" class="mx-auto my-7" />
        </div>
        <div class="p-7">
          <h2 class="text-4xl my-7">{{ product.title }}</h2>
          <p class="text-xl my-7">Price - ${{ product.price }}</p>
          <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
          <div class="description-container" :style="{ 'min-width': '300px' }">
            <p class="mb-7">{{ product.description }}</p>
          </div>
          <button class="btn flex">
            <i class="material-icons mr-2">add_shopping_cart</i>
            <span>Add to cart</span>
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    const { product } = defineProps(['product'])
  </script>
  
  <style scoped>
    img {
      max-width: 300px;
    }
  
    @media screen and (min-width: 640px) {
      img {
        max-width: 50%;
      }
      .description-container {
        min-width: 350px;
      }
    }
  </style>