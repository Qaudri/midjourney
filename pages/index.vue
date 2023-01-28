<template>
  <div class="select-none">
    <section class="hero-bg relative w-full">
      <NavigationHeader class="absolute top-0"></NavigationHeader>
      <div class="mx-auto max-w-7xl h-screen-80 lg:h-screen items-center px-6 md:px-8 lg:px-10 flex">
        <div class="w-full md:w-2/3 lg:w-1/2">
          <h1 class="text-white text-4xl md:text-5xl font-bold leading-10 md:leading-[3.5rem]">Shop the Best Selection of Shoes for Everyone</h1>
          <p class="text-white text-sm lg:text-base 2xl:text-xl mt-0">Where style meets comfort in every step.</p>

          <div class="flex gap-5 mt-5 items-center">
            <UiButtonsPrimary>Download our app</UiButtonsPrimary>
          </div>
        </div>
      </div>
    </section>

    <section class="mx-auto max-w-7xl px-6 md:px-8 lg:px-10 py-20 bg-zinc-100">
      <div class="flex gap-5 overflow-hidden">
        <Shoes v-for="(shoe, index) in shoes" :index="index" :shoe_item="shoe" :key="shoe.id" :shoeName="shoe.name" :shoePrice="shoe.price" :backgroundImagePath="shoe.image" />
      </div>
    </section>
  </div>
</template>

<script>
import vaporBlazer from '@/assets/images/01.jpg'
import AirVision from '@/assets/images/02.jpg'
import CourtJordan from '@/assets/images/03.jpg'
import Ibrahim from '@/assets/images/04.jpg'
import Ibro from '@/assets/images/05.jpg'

export default {
  data(){
    return {
      shoes: [
        {
          id: 1,
          name: 'Vapor Blazer',
          price: 129,
          image: vaporBlazer
        },

        {
          id: 2,
          name: 'Air Vision',
          price: 224,
          image: AirVision
        },

        {
          id: 3,
          name: 'Court Jordan',
          price: 99,
          image: CourtJordan
        },

        {
          id: 4,
          name: 'Ibrahim',
          price: 9,
          image: Ibrahim
        },

        {
          id: 5,
          name: 'Ibro',
          price: 5,
          image: Ibro
        },

        {
          id: 6,
          name: 'High Bee',
          price: 1,
          image: CourtJordan
        },

        {
          id: 7,
          name: 'Vapor Plazer',
          price: 140,
          image: vaporBlazer
        },

        {
          id: 8,
          name: 'Bapor Plazer',
          price: 200,
          image: vaporBlazer
        },

        {
          id: 9,
          name: 'Bapor Plazer',
          price: 350,
          image: vaporBlazer
        },
      ]
    }
  }
}
</script>

<style>
body{
  font-family: Poppins;
}

.hero-bg {
  background: url('../assets/images/bg.jpg');
  background-size: cover;
  background-position: center;
}
</style>