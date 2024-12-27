<template>
    <div class="md:mt-[8rem] text-[0.9rem] font-[Arial] mx-5 mt-[2rem]">
        <div>
             <div class="w-[0%] h-[1px]  bg-black copy-line  dark:bg-white " />
       </div>

       <div class="mt-[3rem] mb-[4rem] md:flex-row flex-col flex gap-6 justify-between">
        <div class="copy-text opacity-0 text-balance  text-center md:text-justify">A COLLABORATIVE PROCESS BETWEEN OZENUA AND CENTURY LEAP</div>
        <h2 class="copy-text opacity-0 flex justify-end">OLAMIDE ADEYI. C 2022</h2>
       </div>
    </div>
</template>

<script setup>
 import gsap from 'gsap';
 import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to('.copy-line',{
         width: '100%',
         duration:1.5,
         scrollTrigger:{
            trigger:'.copy-line',
            start:'top 90%',
         
         }
    })

    gsap.to('.copy-text',{
         opacity:1,
         delay:0.8,
         duration:1.5,
         stagger:0.3,
         scrollTrigger:{
            trigger:'.copy-text',
            start:'top 90%',
         
         }
    })

})
</script>

<style lang="scss" scoped>

</style>