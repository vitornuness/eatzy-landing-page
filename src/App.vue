<script setup>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import DescobrirRestaurantes from './components/DescobrirRestaurantes.vue';
</script>

<template>
  <Header />

  <main>
    <Hero />
    <About />
    <DescobrirRestaurantes />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
