<script setup>
import { ref } from 'vue'

const bio = ref({
  name: 'Ruby Benitez',
  avatar: 'https://api.dicebear.com/9.x/fun-emoji/svg?seed=Brian',
  about:
    'Edinburg-based Special Ed. Teacher and Computer Science student passionate about cybersecurity, creativity, and the journey toward becoming a private chef',
  skills: [
    'Cyber Security Fundementals',
    'Database Management (SQL)',
    'Python Programming',
    'Technical Troubleshooting',
  ],
  email: 'benitez.ruby1@yahoo.com',
  location: 'Edinburg, Tx',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
    <RouterLink
      to="/"
      class="my-8 self-start text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
    >
      ← Back To Links
    </RouterLink>

    <!-- Profile Card -->
    <div
      class="2xl w-full max-w-lg rounded border-gray-700 bg-gray-800 p-6 shadow-xl shadow-gray-900/50 sm:p-8"
    >
      <!-- Header -->
      <div class="mb-6 flex flex-col items-center text-center sm:flex-row sm:text-left"></div>
    </div>
  </main>
</template>
