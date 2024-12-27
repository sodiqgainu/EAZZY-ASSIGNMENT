<template>
    <section class="font-[moglan] text-[6vw] text-center">
        <div class="overflow-hidden">
           <span>Communication</span>
        </div>

        <div class="overflow-hidden ">
           <span>Teamplayer</span>
        </div>

        <div class="overflow-hidden">
           <span>Empathy</span>
        </div>

        <div class="overflow-hidden">
           <span>Creative</span>
        </div>

        <div class="overflow-hidden">
           <span>Critical thinker</span>
        </div>

        <div class="overflow-hidden">
           <span>Figma</span>
        </div>

        <div class="overflow-hidden">
           <span>Adobe XD</span>
        </div>

        <div class="overflow-hidden">
           <span>Adobe Illustrator</span>
        </div>

        <div class="overflow-hidden">
           <span>Adobe Premier Pro</span>
        </div>

        <div class="overflow-hidden">
           <span>Trello</span>
        </div>
    </section>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)


onMounted(() => {
    const span = document.querySelectorAll('span')
    span.forEach((el) =>{
      gsap.to(el,{
        opacity:1,
        y:'0px',
        duration:1.5,
        scrollTrigger:{
            trigger:el.parentElement,
            start:'top 95%',
            bottom:'bottom top',
           
        }
      })
    })
})
</script>

<style lang="postcss" scoped>
span{
    
    @apply inline-block opacity-0 translate-y-[200px] text-nowrap
}
</style>