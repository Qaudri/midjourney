<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>
  import './assets/css/tailwind.css'
  useHead({
    title: `Midjourney | The AI platform that'll change your outlook on life`,
  });
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
body {
  font-family: Poppins sans-serif;
  scroll-behavior: smooth;
}

*::-webkit-scrollbar {
  width:10px;
  background-color: #f7f7f7;
}

*::-webkit-scrollbar-thumb {
  width:5px;
  background-color: #845EC2;
  border-radius: 15px;
}

*::-webkit-scrollbar-thumb:hover {
  background-color: #FF9671;
  transition: ease-in-out;
  transition-duration: .5s;
}
</style>
