<template>
  <section id="concerts" class="py-20 bg-rock-800">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl mb-12 text-center">World Tour <span class="text-rock-accent">2026</span></h2>
      <div class="max-w-4xl mx-auto space-y-4">
        <div v-for="show in tour" :key="show.id" class="flex flex-col md:flex-row items-center justify-between p-6 bg-rock-900 border-l-4 border-rock-accent hover:bg-rock-700 transition-colors group">
          <div class="text-center md:text-left mb-4 md:mb-0">
            <div class="text-rock-accent font-bold text-xl">{{ show.date }}</div>
            <div class="text-gray-500 uppercase text-xs">{{ show.venue }}</div>
          </div>
          <div class="text-2xl font-rock text-white tracking-widest uppercase mb-4 md:mb-0">
            {{ show.city }}, {{ show.country }}
          </div>
          <div>
            <button :disabled="show.soldOut" class="px-6 py-2 font-bold uppercase tracking-tighter transition-all" :class="show.soldOut ? 'bg-gray-700 text-gray-500 cursor-not-allowed' : 'bg-white text-black hover:bg-rock-accent hover:text-white'">
              {{ show.soldOut ? 'Sold Out' : 'Tickets' }}
            </button>
          </div>
        </div>
      </div>
      <p class="text-center mt-12 text-gray-500 italic text-sm">More dates to be announced soon...</p>
    </div>
  </section>
</template>

<script setup>
const tour = [
  { id: 1, date: 'MAR 12', city: 'Paris', country: 'FR', venue: 'L\'Olympia', soldOut: true },
  { id: 2, date: 'MAR 15', city: 'London', country: 'UK', venue: 'Wembley Arena', soldOut: false },
  { id: 3, date: 'MAR 22', city: 'Berlin', country: 'DE', venue: 'Mercedes-Benz Arena', soldOut: false },
  { id: 4, date: 'APR 05', city: 'New York', country: 'USA', venue: 'Madison Square Garden', soldOut: true },
  { id: 5, date: 'APR 12', city: 'Tokyo', country: 'JP', venue: 'Budokan', soldOut: false },
  { id: 6, date: 'MAY 20', city: 'São Paulo', country: 'BR', venue: 'Allianz Parque', soldOut: false }
]
</script>
