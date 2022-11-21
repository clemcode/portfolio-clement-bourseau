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
    <header class="cv-block-header">
      <div class="cv-block-header-wrapper">
        <p class="font-bold">{{ poste }}</p>
        <p class="flex-end">{{ periode }}</p>
      </div>
      <p>{{ entreprise }}</p>
    </header>
    <slot />
  </article>
</template>

<style scoped>
.cv-block-header {
  display: block; 
  padding: 0.25rem; 
  padding-right: 1rem; 
  background-color: #E5E7EB; 
  border-radius: 0.375rem; 
}

.dark .cv-block-header {
  background-color: #1F2937; ;
}

.cv-block-header-wrapper {
  display: flex; 
  justify-content: space-between; 
}

.font-bold {
  font-weight: bold; 
}

.flex-end {
  text-align: right; 
}
</style>