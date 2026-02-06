<template>
  <section class="relative h-screen flex items-center justify-center overflow-hidden">
    <!-- Background Image with Overlay -->
    <div 
      class="absolute inset-0 bg-cover bg-center z-0" 
      style="background-image: url('https://images.unsplash.com/photo-1470225620780-dba8ba36b745?auto=format&fit=crop&q=80&w=1920')"
    >
      <div class="absolute inset-0 bg-black/60"></div>
    </div>

    <div class="relative z-10 text-center px-4">
      <h1 class="text-6xl md:text-9xl mb-4 animate-pulse text-white">
        The Binary <span class="text-rock-accent">Lobsters</span>
      </h1>
      <p class="text-xl md:text-2xl mb-8 font-light tracking-widest text-gray-300">
        ELECTRO-ROCK REVOLUTION // TOUR 2026
      </p>
      <a href="#concerts" class="bg-rock-accent hover:bg-red-700 text-white px-8 py-3 rounded-none transition-all duration-300 uppercase font-bold tracking-widest">
        Get Tickets
      </a>
    </div>

    <div class="absolute bottom-10 left-1/2 -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
      </svg>
    </div>
  </section>
</template>
