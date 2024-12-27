<template>
  <button @click="theme.toggleTheme" data-cursor="-icon" >
    <NuxtImg v-if="theme.theme === 'light'" src="blackTheme.png" width="18px" height="18px" />
    <NuxtImg v-else src="whiteTheme.png" width="18px" height="18px"  />
  </button>
</template>

<script setup>
import { useThemeStore } from '~/store';


const theme = useThemeStore()

</script>

<style lang="scss" scoped>

</style>