<template>
    <main>
      <section class="text-center">
        <div class="hero-container">
          <div class="hero-container__cta">
            <h1 class="main-title">
              Clément Bourseau
            </h1>
            <p class="subtitle">
              Modélisation 3D
            </p>
            <NuxtLink
              class="hero-container__cta__link"
              to="/portfolio/3d/bouclier"
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
  display: flex;
  justify-items: center;
  align-items: center;
  flex-direction: column;
  padding-top: 64px;
}

.hero-container__cta {
  background-color: rgba(0,0,0,.5);
  padding: 1rem;
}

.hero-container__cta__link {
  background-color: rgb(9 35 66);
  color: white;
  font-weight: bold;
  padding: 12px;
  border-radius: 8px;
}

header > div > div:nth-child(0n+3) a {
  display: none;
}

footer {
  display: none;
}

.text-center {
  text-align: center;
}

.main-title {
  font-weight: bold;
  font-size: 24px;
  margin-bottom: 16px;
  color: white;
}

.subtitle {
  margin-bottom: 2.5rem; 
  color: #E5E7EB; 
}

img {
  max-width: 1080px;
  margin: 0 auto!important;
}

@media (max-width: 1080px) {
  img {
    max-width: 100%;
  }
}
</style>