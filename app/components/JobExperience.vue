<template>
    
      <section class="  mx-5 md:mt-[8rem] mt-[3rem] py-3   ">
       <div>
             <div class="w-[0%] h-[1px]  bg-black grade-line  dark:bg-white " />
       </div>
       <div class="grid grid-cols-8 mt-[5rem]  md:gap-4 gap-8">
            <div class='md:col-span-2 col-span-8'>
                <h4>/JOB EXPERIENCE</h4>
            </div>
            <div class="  md:col-span-6 col-span-8">
                <div class="w-[90%] grid grid-cols-6 gap-8 justify-between " >
                <Grade/>
                <Date/>
                </div>
                 <div class="md:w-[90%] w-[100%] mt-[10rem]">
                    <ClipImage/>
                    
                 </div>
            </div>
    </div>
   </section>
</template>

<script setup>
 import gsap from 'gsap';
 import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to('.grade-line',{
         width: '100%',
         duration:1.5,
         scrollTrigger:{
            trigger:'.grade-line',
            start:'top 90%',
          
         }
    })
})
</script>

<style lang="scss" scoped>

</style>