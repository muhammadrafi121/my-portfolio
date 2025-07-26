<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import About from './components/About.vue'
import Works from './components/Works.vue'
import Tools from './components/Tools.vue'
import Contact from './components/Contact.vue'
</script>
<template>
  <div class="container mx-auto pb-20 lg:max-w-3/5">
    <Navbar />
    <About />
    <Works />
    <Tools />
    <Contact />
  </div>
</template>

<style>
body {
  font-family: 'Cutive Mono', sans-serif;
  color: white;
  background-color: #393e46;
}

.container {
  background-color: #222831;
}

.contact-btn {
  stroke: white;
}
</style>
