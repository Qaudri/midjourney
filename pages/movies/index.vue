<script setup lang="ts">
  import { ref } from "vue";
  const shows = ref([]);
  const search = ref("");
  const URL= "https://api.tvmaze.com/search/shows?q=";


  async function searchForMovie(search){
    const grabData = await fetch(URL + search.value)
    const json = await grabData.json()
    shows.value = json
  }

  async function submit(){
    if(!search.value) return
    searchForMovie(search)
  }
</script>
<template>
  <div class="bg-black bg-opacity-90 px-10 py-20 min-h-screen">
    <form @submit.prevent="submit()" class="flex items-center gap-0">
      <input type="text" v-model="search" class="text-white border-white px-4 py-2 bg-white bg-opacity-10 ring-0 outline-0 w-2/3 mx-auto flex rounded-md">
      <UiButtonsPrimary class="mx-0">Search</UiButtonsPrimary>
    </form>

    <div class="grid grid-cols-3 gap-10">
      <Movies v-for="show in shows" :show="show" :key="show.id" class="mt-20" :imagePath="show.show.image ?.medium" :title="show.show.name" :score="show.show.score"></Movies>
    </div>

  </div>
</template>
<style>

</style>