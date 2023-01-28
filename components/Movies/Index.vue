<template>
  <nuxt-link :to="'/results/' + show.show.id" target="_blan" class="flex gap-5 p-5 bg-white bg-opacity-10 rounded-md items-center">
    <img :src="imagePath" class="w-36" alt="">
    <div>
      <h1 class="text-2xl font-medium text-white">{{ title }}</h1>
      <p class="text-white text-sm font-normal">{{ details }}</p>
      <p class="text-white text-sm font-normal">{{ score }}</p>
    </div>
  </nuxt-link>
</template>

<script>
  export default {
    props: {
      imagePath: String,
      title: String,
      details: String,
      show: {
        title: String,
        default: 'Movie',
        type: Object
      },
      score: String
    }
  }
</script>