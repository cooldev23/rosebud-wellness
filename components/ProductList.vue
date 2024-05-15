<template>
  <div>
    <section>
      <ul role="list" class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3">
        <li v-for="product in products.body" :key="product.id"
          class="col-span-1 flex flex-col divide-y divide-gray-200 rounded-lg bg-white text-center shadow-md">
          <div class="flex flex-1 flex-col p-8">
            <!-- <img class="mx-auto h-32 w-32 flex-shrink-0 rounded-full" :src="person.imageUrl" alt="" /> -->
            <h3 class="mt-6 text-xl font-bold text-gray-900">{{ product.name }}</h3>
            <dl class="mt-1 flex flex-grow flex-col justify-between">
              <dt class="sr-only">Title</dt>
              <dd class="text-sm text-gray-600">{{ product.description }}</dd>
              <dt class="sr-only">Role</dt>
              <!-- <dd class="mt-3">
                <span
                  class="inline-flex items-center rounded-full bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">{{
                  product.role }}</span>
              </dd> -->
            </dl>
          </div>
          <div>
            <div class="-mt-px flex">
              <div class="flex w-0 flex-1">
                <NuxtLink :to="`products/${product.id}`"
                  class="relative -mr-px inline-flex w-0 flex-1 items-center justify-center gap-x-3 rounded-bl-lg border border-transparent py-4 text-sm font-semibold text-gray-900">
                  <EnvelopeIcon class="h-5 w-5 text-gray-400" aria-hidden="true" />
                  View Details
                </NuxtLink>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
import { EnvelopeIcon, PhoneIcon } from '@heroicons/vue/20/solid';

const products = await queryContent('/products').findOne();
</script>