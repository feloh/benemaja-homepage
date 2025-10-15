<template>
  <section id="products" class="py-16">
    <v-container>
      <div class="text-center mb-10">
        <h2 class="section-title mb-4">Unsere Produkte</h2>
        <p class="section-subtitle">
          Entdecke die beliebtesten Pflegeprodukte aus unserer Naturkosmetik-Manufaktur.
        </p>
      </div>
      <v-row>
        <v-col v-for="product in products" :key="product.name" cols="12" sm="6" md="4">
          <v-card class="pa-4" elevation="4">
            <v-img :src="product.image" :alt="product.name" height="200" class="rounded-lg" cover />
            <v-card-title class="px-0 mt-4">{{ product.name }}</v-card-title>
            <v-card-text class="px-0">
              <p class="mb-4">{{ product.description }}</p>
              <div class="d-flex align-center justify-space-between">
                <span class="text-h6 font-weight-bold">{{ product.price }}</span>
                <v-btn color="secondary" variant="outlined">Details</v-btn>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script setup>
const products = [
  {
    name: 'Honig-Lavendel Balsam',
    description: 'Beruhigender Pflegebalsam für trockene Haut, angereichert mit Bio-Honig und Lavendelöl.',
    price: 'CHF 24.00',
    image: 'https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?auto=format&fit=crop&w=900&q=80',
  },
  {
    name: 'Wildrosen Gesichtsöl',
    description: 'Vitalisierendes Gesichtsöl mit Wildrosen- und Jojobaöl für einen strahlenden Teint.',
    price: 'CHF 32.00',
    image: 'https://images.unsplash.com/photo-1612810806695-30ba0b39def5?auto=format&fit=crop&w=900&q=80',
  },
  {
    name: 'Zitronenmelisse Body Butter',
    description: 'Leichte Körperbutter mit Shea und Zitronenmelisse für samtweiche Haut.',
    price: 'CHF 28.00',
    image: 'https://images.unsplash.com/photo-1585386959984-a4155224a1ad?auto=format&fit=crop&w=900&q=80',
  },
];
</script>
