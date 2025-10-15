<template>
  <v-app>
    <app-header />
    <v-main>
      <hero-section />
      <parallax-section />
      <about-section />
      <products-section />
    </v-main>
    <app-footer />
  </v-app>
</template>

<script setup>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AboutSection from './components/AboutSection.vue';
import HeroSection from './components/HeroSection.vue';
import ParallaxSection from './components/ParallaxSection.vue';
import ProductsSection from './components/ProductsSection.vue';
</script>
