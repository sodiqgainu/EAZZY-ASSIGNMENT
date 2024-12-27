<template>
    <div class="date-cont font-[Arial]  col-span-3  items-end  flex flex-col" data-cursor="-icon">
         <div class=" h-full grid place-content-center">
            <h1 class="date-text translate-x-[-100%] opacity-0">2022.</h1>
         </div>
         <div  class=" h-full grid place-content-center">
            <h1 class="date-text translate-x-[-100%] opacity-0 ">2021 - 2022</h1>
         </div>
         <div class=" h-full grid place-content-center">
            <h1  class="date-text translate-x-[-100%] opacity-0">2021 - 2022</h1>
         </div>
         <div class=" h-full  grid place-content-center">
            <h1 class="date-text translate-x-[-100%] opacity-0">2019</h1>
         </div>
    </div>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)


onMounted(() => {
    gsap.to('.date-text',{
        x:"0%",
        opacity:1,
        stagger:0.2,
        duration:1.5,
        delay:0.5,
        ease:'power3.inout',
        scrollTrigger:{
            trigger:'.date-cont',
            start:'top, 90%',
           
        }
    })
})
</script>

<style lang="postcss" scoped>
    h1{
        @apply text-[1rem] md:text-[1vw]
    }
</style>