<template>
  <div>
    <div class="h-48 w-80 rounded-t-xl" style="background-position: center; background-size: cover;" :style="{ backgroundImage: `url(${backgroundImagePath})` }"></div>
    <div class="p-5 w-full bg-white rounded-b-xl">
      <div class="flex items-center justify-between">
        <div>
          <h1 class="text-2xl font-medium text-black">{{shoeName}}</h1>
          <p class="text-gray-400 text-sm">{{ShoeCategory}}</p>
        </div>
        <h1 class="text-lg font-normal">${{shoePrice}}</h1>
      </div>
      
      <NuxtLink :to="'/shoes/' + shoeName" target="_blank">
        <UiButtonsPrimary :flexdisplay="true" class="mt-8 w-full">More details</UiButtonsPrimary>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    backgroundImagePath: String,
    shoeName: String,
    shoePrice: Number,
    ShoeCategory: {
      default: 'Shoe Category',
      type: String
    },
    shoe_item: {
      title: String,
      default: 'Shoe Item',
      type: Object
    },
    index: Number
  },
}
</script>

<style>

</style>