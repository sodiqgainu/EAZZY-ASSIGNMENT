<template>
    <div class="clip-img sm:h-[80vh] h-[40vh] max-w-[100%] -[20px] shadow-md">
        <img src="/uba2.jpg" class="w-full h-full object-fill clip-image rounded-[20px]"/>
    </div>
</template>

<script setup>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to('.clip-img',{
   
     ease:'power1.in',
      scale:1,
       
        scrollTrigger:{
            trigger:'.clip-img',
            start:'top, 40%',
            end:'+=100%',
          
        }
    })
})

</script>

<style lang="css"  scoped>
.clip-img {
 transform: scale(0.5);
 border-radius: 20px;
}


</style>