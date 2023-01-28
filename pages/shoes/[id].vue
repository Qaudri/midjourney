<template>
  <div>
    <p>The name of the shoe is {{ $route.params.id }}</p>
  </div>
</template>

<script>
 export default {
    data() {
      return {
        shoe_item: {}
      }
    },

    created() {
      console.log(this.$route.params.id)
    },
 }
</script>

<style>

</style>