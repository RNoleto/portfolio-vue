<script setup>
import Header from './components/Header.vue';
import Hero from './views/Hero.vue';
import AboutMe from './views/AboutMe.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header />
  <main class="AppBody">
    <Hero/>
    <AboutMe/>
  </main>
  <Footer />
</template>

<style scoped></style>
