<script setup>
import HeroSection from './components/HeroSection.vue';
import NavBar from './components/NavBar.vue';
import { defineAsyncComponent } from 'vue';
import ServiceSection from './components/ServiceSection.vue';
import DownloadSvg from './components/icons/downloadSvg.vue';



</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar/>
    <HeroSection/>
    <ServiceSection/>

  </div>
</template>

<style scoped>

</style>
