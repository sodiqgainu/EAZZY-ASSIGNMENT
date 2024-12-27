<template>
      <section class="  mx-5 md:mt-[8rem] mt-[3rem] py-3   ">
       <div>
             <div class="w-[0%] h-[1px]  bg-black contact-line  dark:bg-white " />
       </div>
       <div class="grid grid-cols-8 mt-[5rem]  md:gap-4 gap-8">
            <div class='md:col-span-2 col-span-8'>
                <h4>/CONTACT ME</h4>
            </div>
            <div class="  md:col-span-6 col-span-8 grid justify-center grid-cols-2  font-[Arial] ">
                
                  <div class="flex flex-col md:text-[2.5vw] text-[1.5rem] ">
                     <a href="">BEHANCE</a>
                     <a href="">TWITTER</a>
                     <a href="">GMAIL</a>
                     <a href="">INSTAGRAM</a>
                     <a href="">LINKEDIN</a>
                  </div>
                    
                  <div class=" flex justify-end ">
                    <a href="resume.pdf" download="">DOWNLOAD RESUME</a>
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
    gsap.to('.contact-line',{
         width: '100%',
         duration:1.5,
         scrollTrigger:{
            trigger:'.contact-line',
            start:'top 90%',
          
         }
    })
})
</script>

<style  scoped>

</style>