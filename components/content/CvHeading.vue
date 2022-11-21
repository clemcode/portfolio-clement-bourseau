<template>
  <div class="cv-heading">
    <slot />
  </div>
</template>

<style scoped>
.cv-heading {
  padding: 1rem; 
  margin-bottom: 0.5rem; 
  background-color: #E5E7EB; 
  border-radius: 0.25rem; 
}

.dark .cv-heading {
  background-color: #1F2937;
}
</style>