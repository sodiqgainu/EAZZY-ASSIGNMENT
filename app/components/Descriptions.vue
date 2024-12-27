<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)



onMounted(() => {
    const text1 = document.querySelectorAll('.text1')
    const text2 = document.querySelectorAll('.text2')

    const tl1 = gsap.timeline({
        scrollTrigger:{
            trigger: text1,
            start: 'top bottom',
        }
    })

    tl1.from(text1,{
        y:100,
     
        duration:0.7,
        stagger:0.2
    })

    const tl2 = gsap.timeline({
        scrollTrigger:{
            trigger: text2,
            start: 'top bottom',
           
        }
    })

    tl2.from(text2,{
        y:100,
    delay:0.3,
        duration:0.7,
        stagger:0.3
    })
})
</script>

<template>

    <section class="   w-[90%]  ">
    <div class=" uppercase w-full flex flex-col gap-[6rem]" data-cursor="-big"  >

        <div class="block md:hidden">
            SELF-MOTIVATED DESIGNER WITH WILD
            INTEREST IN CREATING SEAMLESS
            DIGITAL EXPERIENCES.
             
            <br>
            <br>
            <h1 class="uppercase">
             Not only do I believe users' pain
            points can be addressed by a thorough research and design, I
            also believe that it can put a smile
            on the users face.
            </h1>
        </div>
       
        <div class=" md:text-[3vw] text-[3.9vw] text-balance md:block hidden ">
            <div class="overflow-hidden"><h3 class="text1">SELF-MOTIVATED DESIGNER WITH WILD</h3></div>
            <div class="overflow-hidden"><h3 class="text1">INTEREST IN CREATING SEAMLESS</h3></div>
            <div class="overflow-hidden"><h3 class="text1">DIGITAL EXPERIENCES.</h3></div>
        </div>

        <div class="md:text-[3vw] text-[3.9vw] text-balance w-full md:block hidden">
            <div class="overflow-hidden"><h3 class="text2">Not only do I believe users' pain</h3></div> 
            <div class="overflow-hidden"><h3 class="text2">points can be addressed by a </h3></div>
           <div class="overflow-hidden"> <h3 class="text2">thorough research and design, I</h3>  </div>
            <div class="overflow-hidden"><h3 class="text2">also believe that it can put a smile </h3></div>
            <div class="overflow-hidden"><h3 class="text2">on the users face.</h3></div>
        </div>
    </div>
 
    <Image/>
    <MoreInfo/>

    </section>
</template>


<style lang="scss" scoped>

</style>