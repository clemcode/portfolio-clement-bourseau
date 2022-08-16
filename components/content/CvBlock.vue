<script setup>
defineProps({
  poste: String,
  periode: String,
  entreprise: String
})

const isOpen = ref(false)
</script>

<template>
  <article>
    <header class="block rounded-md p-1 bg-gray-200 dark:bg-gray-800 pr-4">
      <div class="flex justify-between">
        <p class="font-bold">{{ poste }}</p>
        <p class="flex-end">{{ periode }}</p>
      </div>
      <p>{{ entreprise }}</p>
    </header>
    <slot />
  </article>
</template>