<template>
  <button @click="$emit('emitMore')" class="font-medium text-sm xl:text-base 2xl:text-xl text-white hover:text-primary ease-in-out duration-500 border-b border-transparent hover:border-primary select-none">
    <slot />
  </button>
</template>

<script>

export default {
  props: {
  }
}
</script>

<style>

</style>