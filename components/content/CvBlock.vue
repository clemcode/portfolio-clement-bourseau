<script setup>
defineProps({
  poste: String,
  description: String,
  periode: String,
  entreprise: String,
  youtubeId: String
})

const isOpen = ref(false)
</script>

<template>
  <div>
    <p>{{ poste }} / <span>{{ entreprise }}</span> <span>{{ periode }}</span></p>
    <p>
      {{ description }}
    </p>
    <div v-if="youtubeId">
      <button @click="isOpen = !isOpen">
        {{ isOpen ? 'Fermer' : 'Afficher' }}
      </button>
      <div v-show="isOpen">
        <iframe 
          :src="'https://www.youtube.com/embed/' + youtubeId" 
          frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen
        />
      </div>
    </div>
  </div>
</template>