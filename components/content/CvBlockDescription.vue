<script setup>
defineProps({
  description: String,
  youtubeId: String
})

const isOpen = ref(false)
</script>

<template>
  <section class="cv-block-description">
    <p>
      {{ description }}
    </p>
    <div v-if="youtubeId" class="youtube-container">
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

<style scoped>
.cv-block-description {
  padding: 0.25rem; 
  margin-bottom: 1rem; 
}

.cv-block-description p {
  margin-bottom: 0.5rem; 
  font-weight: 500; 
}

.cv-block-description .youtube-container {
  font-size: 0.875rem;
  line-height: 1.25rem; 
}
</style>