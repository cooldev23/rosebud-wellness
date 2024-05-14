<template>
  <div>
    <section>
      <ul class="grid grid-cols-1 gap-4">
        <li v-for="product in products.body" :key="product.id" class="p-4 border border-gray-200 rounded-md bg-blue-100 hover:bg-blue-300 hover:shadow-sm font-mono relative shadow-md dark:text-gray-700">
          <div class="flex justify-between items-center">
            <div>
              <a href="#" target="_blank" class="after:absolute after:inset-0">{{ product.name }}</a>
              <p class="mt-1 text-sm">{{ product.description }}</p>
            </div>
            <p>{{ product.id }} *</p>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const products = await queryContent('/products').findOne();
</script>