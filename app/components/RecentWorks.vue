<template>
    <section class="mx-5 py-5  mt-[7rem]">
       <div>
        <div class="w-[0%] h-[1px]  bg-black recent-line  dark:bg-white " />
       </div>
       <div class="grid grid-cols-8   mt-[5rem]  md:gap-8  gap-6 ">
                <div class='md:col-span-2 col-span-6'>
                <h4>/RECENT WORKS</h4>
                </div>
            <div class=" px-5   col-span-8 md:col-span-6  grid gap-[5rem] grid-cols-1 md:grid-cols-2  ">
               
                  <Profile id="1" title1="United Bank of  Africa" title2="Redesign Case study" img="uba.png" class="md:col-span-1 " />
                  <Profile id="2" title1="Digilearn:Defining a" title2="new way to learning" img="https://olamide-gamma.vercel.app/images/Learn-here-light.webp" class="  md:mt-[20vw] " />
                <Profile id="3" title1="Viva Cinema mobile" title2="app case study" img="https://olamide-gamma.vercel.app/images/Pay-me.webp" class="md:-mt-[17vw]"  />
                  <Profile id="4" title1="InSafe Investment " title2="Application" img="https://olamide-gamma.vercel.app/images/Msoft.webp" class="mt-[5rem]" />
           
            </div>
            
       </div>
    </section>
 </template>
 
 <script setup>
 import gsap from 'gsap';
 import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to('.recent-line',{
         width: '100%',
         duration:1.5,
         scrollTrigger:{
            trigger:'.recent-line',
            start:'top 90%',
         }
    })
})

 </script>
 
 <style lang="postcss" scoped>
 
 </style>