<script lang="ts" setup>
const props = defineProps({
  title: String,
  date : String,
})

import TimetableIcon from 'vue-material-design-icons/Timetable.vue'

</script>
<style scoped>

</style>
<template>
    <div class="flex justify-center px-4 sm:px-0 w-80 py-5 sm:w-11/12 lg:w-70">
        <div class="rounded-lg shadow-lg bg-white max-w-sm">
            <a href="#!">
                <img class="rounded-t-lg" src="https://mdbootstrap.com/img/new/standard/nature/184.jpg" alt=""/>
            </a>
        <div class="p-6 space-y-4">
            <p class="text-slate-400 flex flex-row flex-nowrap space-x-2"><TimetableIcon/> <span class="font-bold">{{props.date}}</span></p>
            <h5 class="text-gray-900 text-xl font-bold mb-2">{{ props.title }}</h5>
        </div>
    </div>
</div>
</template>