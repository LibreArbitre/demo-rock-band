<template>
  <section id="band" class="py-20 bg-rock-900">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-4xl mb-16">The <span class="text-rock-accent">Line-up</span></h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div v-for="member in members" :key="member.name" class="group relative overflow-hidden bg-rock-800 p-4 border border-rock-700 hover:border-rock-accent transition-colors">
          <div class="aspect-[3/4] overflow-hidden mb-4">
            <img 
              :src="member.image" 
              :alt="member.name" 
              class="w-full h-full object-cover grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
            >
          </div>
          <h3 class="text-xl mb-1 text-rock-accent">{{ member.name }}</h3>
          <p class="text-gray-500 uppercase text-sm tracking-widest font-bold">{{ member.role }}</p>
          
          <!-- Hover Info Overlay -->
          <div class="absolute inset-x-0 bottom-0 p-6 bg-gradient-to-t from-black to-transparent translate-y-full group-hover:translate-y-0 transition-transform duration-300">
             <p class="text-white text-xs italic">"{{ member.quote }}"</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const members = [
  {
    name: 'Zero One',
    role: 'Lead Vocals & Synth',
    image: 'https://images.unsplash.com/photo-1549413187-052003020555?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80',
    quote: 'Loud is the only language everyone understands.'
  },
  {
    name: 'Solder',
    role: 'Guitar & Effects',
    image: 'https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80',
    quote: 'Feedback is just the guitar talking back.'
  },
  {
    name: 'Kernel',
    role: 'Bass Guitar',
    image: 'https://images.unsplash.com/photo-1594121302421-4d3783a93b37?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80',
    quote: 'The low end holds the world together.'
  },
  {
    name: 'BPM',
    role: 'Drums & Percussion',
    image: 'https://images.unsplash.com/photo-1524230659192-f5f4b00375e8?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80',
    quote: 'Keep the pulse or let it die.'
  }
]
</script>
