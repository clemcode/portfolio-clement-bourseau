<template>
    <main>
      <section class="text-center">
        <div
          class="
            flex
            items-center
            flex-col
            justify-center
            pt-16
            hero-container
          "
        >
          <div class="hero-container__cta">
            <h1 class="font-bold text-3xl mb-4 leading-[1.15] text-white-900">
              Clément Bourseau
            </h1>
            <p class="mb-10 text-gray-500">
              Modélisation 3D
            </p>
            <NuxtLink
              class="
                download-btn
                text-black-500
                font-bold
                px-6
                py-3
                rounded-md
                transition-transform
                hover:scale-105
                hero-container__cta__link
              "
              to="/portfolio/3d/wizard-staff"
              >
                Portfolio
              </NuxtLink>
          </div>
        </div>
      </section>
    </main>
</template>

<style>
.hero-container {
  background-image: url("/img/3d/Sidecar_BMW_R12/Sidecar_BMW_R12_detail_1.png");
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 90vh;
}

.hero-container__cta {
  background-color: rgba(0,0,0,.5);
  padding: 1rem;
}

.hero-container__cta__link {
  background-color: rgb(9 35 66);
}
</style>