<template>
  <div class="max-w-7xl mx-auto w-full">
    <div class="flex items-center mx-auto w-full justify-between px-6 md:px-8 lg:px-10 py-4">
      <div class="w-36">
        <h1 @click="reloadPage()" class="cursor-pointer text-2xl uppercase font-bold text-transparent bg-clip-text bg-gradient-to-br from-primary to-secondary w-40">MidJourney</h1>
      </div>

      <NavigationMenu @revealMenu="toggleMenu()" />

      <nav :class="menu_revealed ? 'translate-x-0' : '-translate-x-full'" class="md:h-fit z-10 md:z-0 md:static md:bg-transparent w-full md:w-fit fixed h-screen left-0 top-[65.5px] md:top duration-500 ease-in-out md:translate-x-0 bg-white">
      <ul class="grid grid-cols-1 place-items-center md:flex gap-5 md:gap-3 lg:gap-5 items-center px-6 pt-20 md:p-0">
        <li class="hidden lg:block">
          <UiButtonsSecondary class="flex gap-2 group items-center">
            <UiIconsSearch class="text-white group-hover:text-primary w-5 h-5 duration-500 ease-in-out"></UiIconsSearch>
            Search
          </UiButtonsSecondary>
        </li>
        <li>
          <UiButtonsSecondary>Projects</UiButtonsSecondary>
        </li>
        <li>
          <UiButtonsSecondary>Marketplace</UiButtonsSecondary>
        </li>
        <li>
          <UiButtonsSecondary @click="toLogin()">Sign In</UiButtonsSecondary>
        </li>
        <li>
          <UiButtonsPrimary @click="toSignUp()">Sign Up</UiButtonsPrimary>
        </li>
      </ul>
      </nav>
    </div>
  </div>

</template>

<script>
export default {
  data() {
    return {
      menu_revealed: false
    }
  },

  methods: {
    toggleMenu(){
      this.menu_revealed = !this.menu_revealed
    },

    reloadPage(){
      return navigateTo('/')
    },

    toLogin(){
      return navigateTo('/login')
    },

    toSignUp(){
      return navigateTo('/signup')
    }
  }
}
</script>

<style>

</style>