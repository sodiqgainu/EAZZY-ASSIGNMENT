<template>
    <section class="mt-[6rem] ">
        <div class="flex justify-between py-3">
            <h1 class="text-[12px] font-[lato]">2020 -  2022</h1>
            <h1 class="text-[12px] font-[lato]">1   /   8</h1>
        </div>
        <div class="flex img-container">
         <div class="overflow-hidden w-full ">
            <NuxtImg src="facedown.png"  class="image1 w-full " />
         </div>
         <div class="overflow-hidden w-full">
            <NuxtImg src="faceup.png" class="image2 w-full" />
         </div>
        </div>
    </section>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)


onMounted(() => {
    const tl = gsap.timeline({
        scrollTrigger:{
            trigger: '.img-container',
            start: 'top 80%',
         
        }
    })

    tl.to('.image1',{
        x:'0%',
        opacity:1,
        duration:2,
        delay:0.2,
        ease:'power3.inOut'
    })
    tl.to('.image2',{
        x:'0%',
        opacity:1,
        duration:2,
        delay:0.2,
        ease:'power3.inOut'
    },'0')
})


</script>

<style  scoped>
.image1{
    transform: translateX(-100%);
    opacity:0;
}
.image2{
    transform: translateX(-100%);
    opacity:0;
}
</style>