<template>
  <section class="p-8 md:p-16 bg-gradient-to-b from-blue-900 to-black text-white min-h-screen">
    <h2 class="text-4xl font-bold text-center mb-8 text-blue-300">Projects</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="bg-black bg-opacity-50 p-6 rounded-lg shadow-lg hover:bg-blue-800 transition duration-300"
      >
        <img :src="project.image" alt="Project Image" class="w-full h-48 object-cover rounded-lg mb-4" />
        <h3 class="text-2xl font-semibold text-blue-400">{{ project.title }}</h3>
        <p class="text-gray-300 mt-2">{{ project.description }}</p>
        <NuxtLink :to="`/projects/${project.id}`" class="text-blue-300 mt-4 inline-block hover:underline">
          See More
        </NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    id: 1,
    title: 'Portfolio Website',
    description: 'My personal portfolio built with Nuxt.js and Tailwind CSS.',
    image: '/images/portfolio-project.jpg' // Path to image
  },
  {
    id: 2,
    title: 'Blog Platform',
    description: 'A markdown-based blog with Nuxt Content module.',
    image: '/images/blog-platform-project.jpg' // Path to image
  },
  {
    id: 3,
    title: 'E-commerce UI',
    description: 'Beautiful shopping UI using Vue and Tailwind CSS.',
    image: '/images/ecommerce-ui-project.jpg' // Path to image
  }
]
</script>

<style scoped>
/* Styling for the projects page */
.bg-gradient-to-b {
  background: linear-gradient(to bottom, #1e3a8a, #000000);
}

.text-blue-300 {
  color: #93c5fd;
}

.text-blue-400 {
  color: #60a5fa;
}

.text-gray-300 {
  color: #d1d5db;
}

.bg-blue-800 {
  background-color: #1e40af;
}

.hover\:bg-blue-800:hover {
  background-color: #1e40af;
}

.w-full {
  width: 100%;
}

.object-cover {
  object-fit: cover;
}
</style>
