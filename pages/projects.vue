<template>
  <section class="p-8 md:p-10 bg-gradient-to-b from-blue-900 to-black text-white min-h-screen">
    <h2 class="text-4xl font-bold text-center mb-8 text-blue-300">Projects</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="bg-black bg-opacity-50 p-2 rounded-lg shadow-lg hover:bg-blue-800 transition duration-300"
      >
        <img :src="project.image" alt="Project Image" class="w-full h-48 object-cover rounded-lg mb-4" />
        <h3 class="text-2xl font-semibold text-blue-400">{{ project.title }}</h3>
        <p class="text-gray-300 mt-2">{{ project.description }}</p>

        <div class="mt-4 flex gap-2">
          <a
            v-if="project.github"
            :href="project.github"
            target="_blank"
            rel="noopener noreferrer"
            class="px-4 py-2 bg-blue-500 hover:bg-blue-600 rounded text-white text-sm"
          >
            GitHub
          </a>
          <a
            v-if="project.figma"
            :href="project.figma"
            target="_blank"
            rel="noopener noreferrer"
            class="px-4 py-2 bg-blue-500 hover:bg-blue-600 rounded text-white text-sm"
          >
            Go to Figma
          </a>
          <a
            v-if="project.demo"
            :href="project.demo"
            target="_blank"
            rel="noopener noreferrer"
            class="px-4 py-2 bg-green-500 hover:bg-green-600 rounded text-white text-sm"
          >
            Live Demo
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    id: 1,
    title: 'Prediksi Penumpang Pesawat',
    description:
      'Proyek pembelajaran mesin untuk memprediksi jumlah penumpang pesawat di beberapa bandara menggunakan data resmi dari BPS (Badan Pusat Statistik) Indonesia. Dibuat dengan Flask untuk aplikasi web dan scikit-learn, XGBoost untuk pelatihan model.',
    image: '/images/ml.png',
    github: 'https://github.com/username/project-penumpang',
    demo: 'https://demo-site.com/project-penumpang'
  },
  {
    id: 2,
    title: '"YUSHARIK" Aplikasi Donasi Masjid',
    description:
      'Proyek pembelajaran untuk donasi ke masjid sekitar kota Padang. Dibuat menggunakan Vue.js dan dengan backend JSON.',
    image: '/images/yusharik.jpeg',
    github: 'https://github.com/adityaAhmadalfarison/yusharik',
    demo: 'https://demo-site.com/yusharik'
  },
  {
    id: 3,
    title: 'Re-Design Gojek',
    description: 'Ujian pembelajaran mendesain ulang aplikasi Gojek. Design UI/UX menggunakan Figma.',
    image: '/images/Figma Gojek.png',
    figma: 'https://www.figma.com/design/sEGIGwe0b5Uzun4u1Czy55/GOJEK-UTS?node-id=1-2&t=UFuKTtIlfAjXlycT-0',
    demo: 'https://figma-demo.com/gojek-redesign'
  },
  {
    id: 4,
    title: 'Re-Desain SPADATI',
    description: 'Proyek tugas besar mendesain ulang Sistem Pembelajaran Daring Teknologi Informasi.',
    image: '/images/Figma SPADATI.png',
    figma: 'https://www.figma.com/design/GcI4HTHyOF0s5ojcF6RasM/Spadati?node-id=400-2593&t=0em3luKtD1zF3WMi-0',
    demo: 'https://www.figma.com/proto/GcI4HTHyOF0s5ojcF6RasM/Spadati?node-id=1-4&t=0em3luKtD1zF3WMi-0&scaling=contain&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=400%3A2593&show-proto-sidebar=1'
  }
]
</script>
