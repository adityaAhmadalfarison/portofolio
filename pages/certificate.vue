<template>
  <section class="p-8 md:p-16 min-h-screen bg-gradient-to-b from-blue-900 to-black text-white">
    <h2 class="text-4xl font-bold text-center mb-8 text-blue-300">Sertifikat Saya</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
      <div
        v-for="(cert, index) in certificates"
        :key="index"
        class="bg-black bg-opacity-50 p-6 rounded-lg shadow-lg hover:bg-blue-800 transition duration-300"
      >
        <img :src="cert.image" :alt="cert.title" class="w-full h-48 object-cover rounded-lg mb-4" />
        <h3 class="text-2xl font-semibold text-blue-400">{{ cert.title }}</h3>
        <p class="text-gray-300 mt-2">{{ cert.description }}</p>
        <a
          v-if="cert.link"
          :href="cert.link"
          target="_blank"
          class="text-blue-300 mt-4 inline-block hover:underline"
        >Lihat Sertifikat</a>
      </div>
    </div>
  </section>
</template>

<script setup>
const certificates = [
  {
    title: 'Web Development Bootcamp',
    description: 'Belajar frontend & backend web development selama 8 minggu intensif.',
    image: '',
    link: 'https://drive.google.com/sertifikat-webdev'
  },
  {
    title: 'Flutter Mobile App',
    description: 'Membuat aplikasi mobile menggunakan Flutter dan Firebase.',
    image: '',
    link: 'https://drive.google.com/sertifikat-flutter'
  },
  {
    title: 'UI/UX Design Fundamentals',
    description: 'Dasar-dasar desain antarmuka pengguna dan pengalaman pengguna.',
    image: '',
    link: 'https://drive.google.com/sertifikat-uiux'
  }
]
</script>

<style scoped>
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
</style>
