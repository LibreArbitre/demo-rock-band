<script setup>
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import BandMembers from './components/BandMembers.vue'
import Concerts from './components/Concerts.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen">
    <!-- Navigation Overlay -->
    <nav class="fixed top-0 w-full z-50 p-6 flex justify-between items-center bg-gradient-to-b from-black/80 to-transparent">
      <div class="text-xl font-rock tracking-tighter">
        <span class="text-white">BINARY</span><span class="text-rock-accent">LOBSTERS</span>
      </div>
      <div class="hidden md:flex gap-8 text-xs font-bold uppercase tracking-widest text-gray-400">
        <a href="#about" class="hover:text-white transition-colors">Legend</a>
        <a href="#band" class="hover:text-white transition-colors">Line-up</a>
        <a href="#concerts" class="hover:text-white transition-colors">Tour</a>
        <a href="#contact" class="hover:text-white transition-colors">Join</a>
      </div>
    </nav>

    <Hero />
    <About />
    <BandMembers />
    <Concerts />
    <Contact />
    <Footer />
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>
