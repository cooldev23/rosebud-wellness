<template>
  <div class="mx-auto max-w-7xl">
    <div class="flex items-center justify-between">
      <div class="flex items-center justify-between">
        <NuxtLink to="/" class="me-4 p-2 text-2xl font-semibold hover:bg-blue-200">Rosebud Wellness</NuxtLink>
        <Menu />
      </div>
      <ClientOnly>
        <ColorModeSelector />
      </ClientOnly>
    </div>
  </div>
  <header class="flex justify-center items-center">
    <p class="text-5xl text-white">Here is Some Grand Text</p>
  </header>
  <main class="mt-10 p-2 max-w-7xl mx-auto">
    <slot />
  </main>
</template>

<script setup>
useHead({
  titleTemplate: '%s - Rosebud Wellness',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Tenor+Sans&family=Roboto&display=swap',
      crossorigin: ''
    }
  ]
})
</script>

<style>
body {
  font-family: 'Tenor Sans';
  @apply bg-gray-100;
}

body {
  @apply bg-gray-100 dark:bg-gray-900 text-gray-700 dark:text-gray-300
}

header {
  background-image: url('~/public/img/header-image.jpg');
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 40rem;
}
</style>