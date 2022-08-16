<script setup>
defineProps({
  description: String,
  youtubeId: String
})

const isOpen = ref(false)
</script>

<template>
  <section class="mb-4 p-1">
    <p class="font-medium mb-2">
      {{ description }}
    </p>
    <div v-if="youtubeId" class="text-sm">
      <button @click="isOpen = !isOpen">
        🖥
        {{ isOpen ? 'Fermer la vidéo ▴' : 'Afficher la vidéo ▾' }}
      </button>
      <div v-show="isOpen">
        <iframe 
          :src="`https://www.youtube.com/embed/${youtubeId}`"
          width="560"
          height="315"
          frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen
        />
      </div>
    </div>
  </section>
</template>