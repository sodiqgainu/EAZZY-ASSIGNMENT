<template>
    <div class="flex flex-col gap-10 items-center justify-start md:text-[1vw] sm:text-[1.5vw] text-[2.5vw] w-[10%]  font-light">
      <div class="flex md:gap-[3.3vw] sm:gap-[5vw] gap-[8vw] flex-col font-normal font-[gt] tracking-widest">
        <h2 class="order-2">SCROLL</h2>
      <h2 class="order-1">DOWN</h2>
      </div>
      <div ref="arrow" class="">
        <NuxtImg v-if="theme.theme === 'light'" src="blackdownArrow.png" width="20px"/>
        <NuxtImg v-else src="whitedownArrow.png" width="20px"/>
      </div>
    </div>
</template>

<script setup>
import { useThemeStore } from '~/store';
import gsap from 'gsap';

const theme = useThemeStore()

const arrow = ref(null)

onMounted(() => {
  gsap.fromTo(arrow.value,{
    y:-5,
    yoyo:true,
    repeat:-1,
    duration:0.7
  },{
    y:10,
    yoyo:true,
    repeat:-1,
    duration:0.7
  })
})

</script>

<style scoped>
 h2{
   transform: rotate(-90deg);
 }
</style>