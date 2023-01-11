<script lang="ts" setup>
const props = defineProps({
  title: String,
  text: String
})
</script>
<style scoped>

</style>
<template>
    <div class="mx-auto space-y-8 font-bold py-24">
        <h1 class="text-center text-2xl">{{ props.title }}</h1>
        <p class="px-5 text-center text-slate-400 max-w-2xl mx-auto">{{ props.text }}</p>
    </div>
</template>