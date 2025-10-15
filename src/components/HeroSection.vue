<template>
  <section id="hero" class="hero-section">
    <v-img
      src="https://images.unsplash.com/photo-1504199367641-4070f0b1f3ae?auto=format&fit=crop&w=1600&q=80"
      cover
      class="hero-image"
    >
      <v-container class="fill-height d-flex flex-column align-center justify-center text-center text-white">
        <h1 class="display-2 font-weight-bold mb-4">Natürliche Pflege von Benemaja</h1>
        <p class="text-h6 mb-6">
          Handgefertigte Naturkosmetik mit Liebe und Achtsamkeit aus ausgewählten Bio-Zutaten.
        </p>
        <div>
          <v-btn color="primary" class="me-4" size="large" @click="scrollTo('products')">
            Sortiment entdecken
          </v-btn>
          <v-btn variant="outlined" color="white" size="large" @click="scrollTo('about')">
            Mehr erfahren
          </v-btn>
        </div>
      </v-container>
    </v-img>
  </section>
</template>

<script setup>
const scrollTo = (target) => {
  const element = document.getElementById(target);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>

<style scoped>
.hero-section {
  position: relative;
  min-height: 100vh;
}

.hero-image {
  min-height: 100vh;
}
</style>
