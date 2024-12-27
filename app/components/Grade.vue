<template>
    <div class="grade-cont font-[Arial] col-span-3" data-cursor="-icon">
         <div class="overflow-hidden">
            <h1 class="grade-text translate-y-[100%] opacity-0">ANTHONIA  AND GRADE</h1>
         </div>
         <div  class="overflow-hidden">
            <h1 class="grade-text translate-y-[100%] opacity-0">CENTURY LEAP</h1>
         </div>
         <div class="overflow-hidden">
            <h1  class="grade-text translate-y-[100%] opacity-0">THEONEOZENUA</h1>
         </div>
         <div class="overflow-hidden">
            <h1 class="grade-text translate-y-[100%] opacity-0">TIMESCAPE MEDIA</h1>
         </div>
    </div>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)


onMounted(() => {
    gsap.to('.grade-text',{
        y:"0%",
        opacity:1,
        stagger:0.2,
        duration:1.5,
        ease:'power2.out',
        scrollTrigger:{
            trigger:'.grade-cont',
            start:'top, 90%',
           
        }
    })
})
</script>

<style lang="postcss" scoped>
h1{
    @apply md:text-[2.5vw] text-[1.5rem] w-full 
}
</style>