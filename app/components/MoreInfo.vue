<template>
    <section class="py-4 flex mt-[4rem] flex-col gap-[3rem]" data-cursor="-icon">
        <div class="flex opacity-0 " ref="text1">
            <h1 class="text-balance md:text-[1.5vw] text-[3vw] w-[475px]" >I am a certified product designer with over 2 years of experience in the design industry. I have designed projects and conducted research on user needs and pain points.</h1>
        </div>

        <div class=" flex justify-center pl-auto md:pl-[10rem] opacity-0 " ref="text2">
            <h1 class="text-balance md:text-[1.5vw] text-[3vw] w-[475px]">and I've always channeled the research towards creating a user friendly product. I believe equity is achievable in design and that accessibility and inclusiveness is for the greater good of all users</h1>
        </div>

        <div class=" flex justify-center opacity-0" ref="text3">
            <h1 class="text-balance md:text-[1.5vw] text-[3vw] w-[475px]">My experience in the industry has made me understand how collaboration and teamwork can make a product a success.</h1>
        </div>
    </section>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

const text1 = ref(null)
const text2 = ref(null)
const text3 = ref(null)

onMounted(() => {
  gsap.to(text1.value,{
    opacity:1,
    duration:1.5,
    delay:1,
    scrollTrigger:{
        trigger:text1.value,
        start:'top bottom',
    }
  })

  gsap.to(text2.value,{
    opacity:1,
    duration:1.5,
    delay:1,
    scrollTrigger:{
        trigger:text2.value,
        start:'top bottom',
    }
  })

  gsap.to(text3.value,{
    opacity:1,
    duration:1.5,
    delay:1,
    scrollTrigger:{
        trigger:text3.value,
        start:'top bottom',
    }
  })
})

</script>

<style lang="scss" scoped>

</style>