<template>
  <div class="h-fit">
    <div class="min-h-[80%]">
      <span
        class="block image shadow-sm"
        :class="`img_container-${id} overflow-hidden `"
        data-cursor="-icon"
      >
        <NuxtImg
          :src="img"
          class="w-full object-cover img scale-[1.1]"
          :class="`profileImg-${id}`"
        />
      </span>
      <div class="mt-4">
        <div class="overflow-hidden ">
          <h1
            class="md:text-[2vw] text-[4vw] translate-y-[100px]"
            :class="`text-hollow-${id}`"
          >
            {{ title1 }}
          </h1>
        </div>
        <div class="overflow-hidden ">
          <h1
            class="md:text-[2vw] text-[4vw] text-hollow translate-y-[100px]"
            :class="`text-hollow-${id}`"
          >
            {{ title2 }}
          </h1>
        </div>
        <span class="flex gap-2 items-center">
          <h1 class="md:text-[1vw] text-[2vw] font-[lato]">see case</h1>
          <div class="md:max-w-[30px] max-w-[20px]">
            <NuxtImg v-if="theme.theme === 'light'" src="blackrightarrow.png" />
            <NuxtImg v-else src="whiterightarrow.png" />
          </div>
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useThemeStore } from '~/store';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger);

const theme = useThemeStore();

const props = defineProps({
  title1: { type: String, required: true },
  title2: { type: String, required: true },
  id: { type: String, required: true },
  img: { type: String, required: true },
});

onMounted(() => {
  const imgCont = document.querySelector(`.img_container-${props.id}`);

  imgCont.addEventListener('mouseover', () => {
    gsap.to(`.profileImg-${props.id}`, {
      scale: 1,
      duration: 1,
      ease: 'power3.inOut',
    });
  });

  imgCont.addEventListener('mouseleave', () => {
    gsap.to(`.profileImg-${props.id}`, {
      scale: 1.1,
      duration: 1,
      ease: 'power3.inOut',
    });
  });

  gsap.fromTo(
    `.profileImg-${props.id}`,
    {
      y: '-10vw',
    },
    {
      scrollTrigger: {
        scrub: true,
        trigger: `.img_container-${props.id}`,
        start: 'top bottom',
        end: 'bottom top',
      },
      y: '10vw',
      ease: 'none',
    }
  );

  gsap.to(`.text-hollow-${props.id}`, {
    y: 0,
    duration: 1,
    scrollTrigger:{
      trigger:`.text-hollow-${props.id}`,
      start: 'top bottom',
      end: 'bottom top',
      
    }
  });
});
</script>

<style lang="postcss" scoped>
.img {
  @apply w-full h-full;
}
.image {
  @apply md:h-[40vw];
}
</style>
