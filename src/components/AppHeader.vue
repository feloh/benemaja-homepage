<template>
  <v-app-bar flat color="transparent" class="app-header" :elevation="isScrolled ? 4 : 0">
    <v-toolbar-title class="text-uppercase font-weight-bold">Benemaja</v-toolbar-title>
    <v-spacer />
    <v-btn variant="text" class="mx-2" @click="scrollTo('hero')">Start</v-btn>
    <v-btn variant="text" class="mx-2" @click="scrollTo('about')">Über uns</v-btn>
    <v-btn variant="text" class="mx-2" @click="scrollTo('products')">Produkte</v-btn>
  </v-app-bar>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue';

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 40;
};

const scrollTo = (target) => {
  const element = document.getElementById(target);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};

onMounted(() => {
  handleScroll();
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.app-header {
  backdrop-filter: blur(8px);
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
}

.app-header.v-app-bar--is-scrolled {
  background-color: rgba(250, 247, 242, 0.9);
}
</style>
