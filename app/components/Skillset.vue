<template>
    <section class="mx-5  mt-[7rem] ">
       <div>
        <div class="w-[0%] h-[1px]  bg-black div-line dark:bg-white " />
       </div>
       <div class="grid grid-cols-6    mt-[5rem]  gap-4  ">
                <div class='md:col-span-2 col-span-6'>
                <h4>/SKILLSET</h4>
            </div>
            <div class="flex header  md:col-span-3 col-span-6 justify-center">
                <Skills/>
            </div>
       </div>
    </section>
 </template>
 
 <script setup>
 import gsap from 'gsap';
 import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to('.div-line',{
         width: '100%',
         duration:1.5,
         scrollTrigger:{
            trigger:'.div-line',
            start:'top 90%',
         }
    })
})

 </script>
 
 <style lang="scss" scoped>
 
 </style>