<script setup>

import gsap from 'gsap';

const props = defineProps({
   title: { type: String,  required: true },
   id: { type: String, required: true }
})


onMounted(() => {
   const stuff = document.querySelector(`.stuff-${props.id}`);
  
      stuff.addEventListener('mouseover', () => {
         const tl = gsap.timeline()

         tl.to(`.link1-${props.id}`,{
            y:'-100%',
         })

         tl.to(`.link2-${props.id}`,{
            y:'0%',
         },'0')
      });

      stuff.addEventListener('mouseleave', () => {
         const tl = gsap.timeline()

         tl.to(`.link1-${props.id}`,{
            y:'0%',
         })

         tl.to(`.link2-${props.id}`,{
            y:'100%',
         },'0')
      });
   
   

})

</script>

<template>
   <ul class="overflow-hidden relative font-[gt] text-[14px] leading-[17.57px] font-[400] " :class="`stuff-${id}`" data-cursor="-icon">
    <li class="absolute inset-0" :class="`link1-${id}`">{{ title }}</li>
    <li class="translate-y-[100%]" :class="`link2-${id}`">{{ title }}</li>
   </ul>
</template>

<style lang="scss" scoped>

</style>