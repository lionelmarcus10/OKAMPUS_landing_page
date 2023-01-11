<script setup lang="ts">
import { ref } from 'vue'
// import vue-material-design-icons
import ArrowRightIcon from 'vue-material-design-icons/ArrowRight.vue'
import ArrowDownIcon from 'vue-material-design-icons/ArrowDown.vue'
import FacebookIcon from 'vue-material-design-icons/Facebook.vue'
import InstagramIcon from 'vue-material-design-icons/Instagram.vue'
import LinkedinIcon from 'vue-material-design-icons/Linkedin.vue'
import Caroussel_1 from './Caroussel_1.vue'
import Caroussel_2 from './Caroussel_2.vue'
import Title from './Title.vue'
import FooterVue from './Footer.vue'
import NewsCardVue from './NewsCard.vue'
import ServiceCard from './ServicesCard.vue'
import '../assets/fonts/style.css'

let Services = "Executive Trade International is an University Application Center, guiding Bangladeshi students to study Australian, British, Canadian and Irish universities!"
let News = "Sunt autem nusquam hox epicurus in gravissimo bello animadversionis metu degendae praesidia firmissima. Torquatos nosotros? quos tu paulo ante cum teneam sententiam"
</script>

<style scoped>
.first_part {
  background: url(../assets/im5.jpg) no-repeat center center;
  background-size: cover;
  height:70em;
}
body{
  
}

button {
  border-radius: 8px;
  border: 1px solid transparent;
  color: white;
  padding: 0.6em 1.2em;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  background-color: #646cff;
  cursor: pointer;
  transition: border-color 0.25s;
  
}
button:hover {
  /*background-color: transparent;;
  color: #646cff;
  border-color: #fff;
  border-width: 4px;
  border-style: double;*/
}

/* media query for background image */
.message-impact{
  font-family: "Gordita Bold", sans-serif;
}
</style>

<template>

  <!-- Navigation-->
 
  <!-- Part 1 -->
  <div class="first_part py-36 sm:py-56 px-8 sm:px-28 md:px-36 space-y-12 lg:px-32 xl:px-[250px] 2xl:px-[350px]">
    <div class="flex flex-col items-start space-y-8 md:space-y-12">
      <p class="message-impact text-xl sm:text-2xl md:text-4xl lg:text-4xl">Framer For StartUps</p>
      <h1 class="w-9/12 text-5xl scale-sm sm:text-7xl -sm:text-slate-50 message-impact md:text-7xl lg:text-8xl">Big <span class="text-blue-500">launch. <br></span> Small team.</h1>
      <p class="py-5 text-white font-medium text-3xl sm:text-4xl md:font-bold max-w-lg">Announce your product with a bang without needing an entire marketing team and months of preparation.</p>
      <button class="flex flex-direction flex-nowrap space-x-2 sticky top-0"> <p class="sticky top-0">Apply Online</p> <ArrowRightIcon/> </button>
    </div>
    <div class="flex flex-row space-x-5">
      <FacebookIcon/>
      <InstagramIcon/>
      <LinkedinIcon/>
    </div>
  </div>

  <!-- Part 2 -->
  <div class="bg-zinc-50 flex flex-col pt-8 pb-16 bg-slate-50">
    <h4 class="text-slate-400 font-bold self-center sm:text-2xl md:pb-12 text-xl  message-impact">FEATURED UNIVERSITIES</h4>
    <div class="py-5">
      <Caroussel_1/>
    </div>
  </div>


  <!-- Part 4 -->

  <div class="flex flex-col items-center bg-zinc-50 sm:px-8 lg:px-36 pb-24">

    <!-- Sous partie 1 -->
    <Title title="News" :text="News"/>

    <div class="space-y-8 md:space-y-12">
        <!-- Sous partie 2 -->
      <div class="place-content-center grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 place-items-center px-12 md:px-16">
        <!-- 3 cards -->
        <NewsCardVue title="Come On In. The Water's Fine (Mostly)" date="17 Apr 2022" class="font-bold" fillcolor="#000" :size="48"/>
        <NewsCardVue title="Come On In. The Water's Fine (Mostly)" date="17 Apr 2022" class="font-bold" fillcolor="#000" :size="48"/>
        <NewsCardVue title="Come On In. The Water's Fine (Mostly)" date="17 Apr 2022" class="font-bold" fillcolor="#000" :size="48"/>
      </div>

      <div class="py-12 flex justify-center">
        <button class="flex flex-direction flex-nowrap space-x-2"> <p>Join Here</p> <ArrowRightIcon/> </button>
      </div>
    </div>
  
  </div>

  <!-- Part 7 -->
  <div class="">

     <!-- Sous partie 1 -->
     <Title title="Testimonial" :text="Services"/>

    <!-- Sous partie 2 -->
    <div class="mx-8 sm:mx-28 md:mx-36 space-y-12 lg:mx-32 xl:mx-[250px] 2xl:mx-[350px] ">
      <!-- caroussel multiple card MANGERKOI style -->
      <Caroussel_2/>
    </div>

  </div>

  <!-- Part 8 Appel à l'action -->
  <div class="mx-auto bg-zinc-100 flex flex-row px-8 space-x-2 sm:px-28 sm:space-x-2 md:pl-36 md:pr-32 xl:px-64 2xl:px-[380px] justify-between py-14">
    <h2 class="font-bold text-xl md:text-3xl">Ready to chase your dreams ? </h2>
    <button class="flex flex-row flex-nowrap space-x-4"> <p class="text-sm">Apply Online</p> <ArrowRightIcon/> </button>
  </div>
  <!-- Formulaire -->
  <div class="">
    
  </div>
  <!-- Footer -->
  <FooterVue/>
</template>

