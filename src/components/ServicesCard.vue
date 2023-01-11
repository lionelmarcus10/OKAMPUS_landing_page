<script lang="ts" setup>
import FacebookIcon from 'vue-material-design-icons/Facebook.vue'
import ArrowRightIcon from 'vue-material-design-icons/ArrowRight.vue'

const props = defineProps({
  icon: String,
  title: String,
  text: String
})

</script>
<style scoped>

</style>
<template>
    <div class="px-4 sm:px-0 w-80 py-5 sm:w-11/12 lg:w-70">
      <!-- 5 cards -->
      <div class="py-8 shadow-inner transition ease-in-out hover:delay-500 sm:shadow-md hover:shadow-sm sm:hover:shadow-xl rounded-lg p-5 font-bold bg-white hover:outline hover:outline-blue-500 hover:outline-offset-0 hover:outline-4 text-left space-y-8">
        <div class="bg-red-500 rounded-full p-4 w-20 h-20"><FacebookIcon :size="48"/></div>
        <div class="flex flex-col space-y-3">
          <h3 class="text-2xl">Carrer Counselling</h3>
          <p class="text-sm text-slate-400">Maiores voluptas laboriosam non dolorum perferendis fuga repellat aut. Blanditiis quos in minus</p>
        </div>
        <span class="flex flex-row space-x-2 text-blue-500"><p>Learn More</p> <ArrowRightIcon/></span>
      </div>
    </div>

   
</template>

<!-- 
<div class="sm:px-8 lg:px-36 pb-24">
  <Title title="Our Services" :text="Services"/>
  <div class="place-content-center grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 place-items-center px-12 md:px-16">
  <ServiceCard/>
  <ServiceCard/>
  <ServiceCard/>
  <ServiceCard/>
  <ServiceCard/>
  </div>
</div> 
-->