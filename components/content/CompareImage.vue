<script setup>
const isClient = ref(false)

const ImgComparisonSlider = defineAsyncComponent(async () => {
  const esModule = await import('@img-comparison-slider/vue/dist/index.esm')

  return  esModule.ImgComparisonSlider
})

onMounted(() => {
  isClient.value = true
})

defineProps({
  first: String,
  second: String,
  firstText: {
    type: String,
    default: 'Maillage'
  },
  secondText: {
    type: String,
    default: 'Diffuse'
  },
})
</script>

<template>
  <div>
    <Transition>
      <ImgComparisonSlider v-if="isClient" class="hover">
        <img
          slot="first"
          style="width: 100%"
          :src="first"
        />
        <img
          slot="second"
          style="width: 100%"
          :src="second"
        />
      </ImgComparisonSlider>
    </Transition>
    <p class="text-center w-100">
      <span>{{ firstText }}</span>
      ⟷
      <span>{{ secondText }}</span>
    </p>
    <p class="text-left w-100">
      <a class="underline" :href="`/hd${first}`" target="_blank" rel="noopener noreferrer">{{ firstText}} HD</a>
      <br />
      <a class="underline" :href="`/hd${second}`" target="_blank" rel="noopener noreferrer">{{ secondText}} HD</a>
    </p>
  </div>
</template>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

.hover {
  cursor: grab;
}
</style>