<template>
  <article class="prose dark:prose-invert">
    {{ product }}
  </article>
</template>

<script setup>
const route = useRoute();
const productId = route.params.slug[0];
const product = await queryContent('/products').where({ id: 1 }).findOne();
</script>