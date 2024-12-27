<template>
   <section class=" flex flex-col  mx-5 mt-[100px] opacity-0 hero-cont" data-cursor="-big">
    <Divider/>
    <h1 class="perse">OLAMIDE ADEYI</h1>
    <Divider/>
    <div class="flex justify-between items-center" >
        <div class="w-[5vw] ">
            <NuxtImg v-if="theme.theme === 'light'" src="blackstar.png" class="w-full" />
            <NuxtImg v-else src="whitestar.png" class="w-full" />
        </div>
        <h1 class="perse">WORKFOLIO</h1>
        <div class="w-[5vw]">
            <NuxtImg v-if="theme.theme === 'light'" src="blackstar.png" class="w-full" />
            <NuxtImg v-else src="whitestar.png" class="w-full" />
        </div>
     
    </div>

    <Divider/>
   </section>
</template>

<script setup>
import gsap from 'gsap';
import { useThemeStore } from '~/store';

const theme = useThemeStore()

onMounted(() => {

    const tl = gsap.timeline()
    
    tl.to('.hero-cont',{
        opacity: 1
    })

    tl.to('.perse',{
       z: '0px',
       duration:1.5,
       rotateX:0,
       opacity:1
    },'0')
   

})

</script>

<style  scoped>
section{
    perspective: 1000px;
}
  
  .perse{
    transform: translateZ(-500px);
    transform: rotateX(-60deg);
    opacity: 0;
  }
  h1 {
		@apply text-[11vw] font-[moglan] xl:text-[13.5vw] uppercase text-center leading-relaxed xl:leading-[18.7vw];
	  }
</style>