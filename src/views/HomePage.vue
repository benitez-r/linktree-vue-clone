<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'RUBY BENITEZ',
  slogan: 'Special Ed. Teacher and Advanced Web Designer',
  avatar: 'https://api.dicebear.com/9.x/fun-emoji/svg?seed=Brian',
  links: [
    {
      id: 1,
      title: 'GitHub',
      url: 'https://github.com/benitez-r',
      icon: 'code',
      description: 'Check out my projects',
    },
    {
      id: 2,
      title: 'Linkedin',
      url: 'https://linkedinbenitez-r',
      icon: 'briefcase',
      description: 'Connect with me professionally',
    },
    {
      id: 3,
      title: 'Expense Splitter',
      url: 'https://expense-splitter-vue.benitez-r.workers.dev/',
      icon: 'calculator',
      description: 'Calculate your expenses using my ExpenseSplitter',
    },
  ],
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header -->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20 sm:h-32 sm:w-32"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
        :title="link.title"
        :url="link.url"
        :description="link.description"
        :icon="link.icon"
      />
    </div>

    <!-- Navigate to Info -->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
      >About Me →</RouterLink
    >
  </main>
</template>
