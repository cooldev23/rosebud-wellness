<template>
  <div class="container">
    <header class="flex justify-between items-center mt-4">
      <div class="mx-auto">
        <div>
          <NuxtLink to="/" class="text-2xl p-2 font-semibold hover:bg-blue-200">Rosebud Wellness</NuxtLink>
        </div>
        <div class="flex items-center">
          <Menu />
          <ClientOnly>
            <ColorModeSelector />
          </ClientOnly>
        </div>
      </div>
    </header>
    <main class="mt-10 p-2">
      <slot />
    </main>
  </div>
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
}
</style>