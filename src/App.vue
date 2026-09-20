<template>
  <div class="frame">
    <Header />
    <Marquee />
    <Hero />
    <Manifesto />
    <Principles />
    <Specs />
    <Modules />
    <BuildLog />
    <Cta />
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Marquee from './components/Marquee.vue'
import Hero from './components/Hero.vue'
import Manifesto from './components/Manifesto.vue'
import Principles from './components/Principles.vue'
import Specs from './components/Specs.vue'
import Modules from './components/Modules.vue'
import BuildLog from './components/BuildLog.vue'
import Cta from './components/Cta.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
.frame {
  min-height: 100vh;
  border: 3px solid var(--ink);
}
</style>
