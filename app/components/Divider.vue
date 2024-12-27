<template>
       <div class="w-[0%] h-[1px]  bg-black line dark:bg-white " />
</template>

<script setup>
import gsap from 'gsap';

onMounted(() => {
    gsap.to('.line',{
         width: '100%',
         duration:1.5
    })
})

</script>

<style lang="scss" scoped>

</style>