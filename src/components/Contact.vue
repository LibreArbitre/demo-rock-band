<template>
  <section id="contact" class="py-20 bg-rock-900">
    <div class="container mx-auto px-4 max-w-2xl text-center">
      <h2 class="text-4xl mb-4">Join the <span class="text-rock-accent">Horde</span></h2>
      <p class="text-gray-500 mb-12">Leave a message for the lobsters or inquire about booking.</p>
      
      <form @submit.prevent="handleSubmit" class="space-y-6 text-left">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <label class="block text-xs uppercase text-gray-500 mb-2 font-bold tracking-widest">Name</label>
            <input type="text" class="w-full bg-rock-800 border-b-2 border-rock-700 p-3 focus:outline-none focus:border-rock-accent transition-colors text-white" required>
          </div>
          <div>
            <label class="block text-xs uppercase text-gray-500 mb-2 font-bold tracking-widest">Email</label>
            <input type="email" class="w-full bg-rock-800 border-b-2 border-rock-700 p-3 focus:outline-none focus:border-rock-accent transition-colors text-white" required>
          </div>
        </div>
        <div>
          <label class="block text-xs uppercase text-gray-500 mb-2 font-bold tracking-widest">Subject</label>
          <select class="w-full bg-rock-800 border-b-2 border-rock-700 p-3 focus:outline-none focus:border-rock-accent transition-colors text-white">
            <option>Booking Inquiry</option>
            <option>Press & Media</option>
            <option>Fan Message</option>
            <option>Other</option>
          </select>
        </div>
        <div>
          <label class="block text-xs uppercase text-gray-500 mb-2 font-bold tracking-widest">Message</label>
          <textarea rows="5" class="w-full bg-rock-800 border-b-2 border-rock-700 p-3 focus:outline-none focus:border-rock-accent transition-colors text-white" required></textarea>
        </div>
        <button type="submit" class="w-full bg-rock-accent hover:bg-red-700 text-white font-bold py-4 uppercase tracking-widest transition-all">
          {{ sent ? 'Message Received' : 'Transmit Signal' }}
        </button>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
const sent = ref(false)
const handleSubmit = () => {
  sent.value = true
  setTimeout(() => sent.value = false, 3000)
}
</script>
