<script setup>
import HeroSection from './components/HeroSection.vue';
import NavBar from './components/NavBar.vue';
import { defineAsyncComponent } from 'vue';
import ServiceSection from './components/ServiceSection.vue';
import DownloadSvg from './components/icons/downloadSvg.vue';
import AboutSection from '@/components/AboutSection.vue';
import ExperienceAndSkills from './components/ExperienceAndSkills.vue';
import LatestProjSection from './components/LatestProjSection.vue';
import ContactSection from './components/ContactSection.vue';
import TestimonialsSection from './components/TestimonialsSection.vue';
import FooterSection from './components/FooterSection.vue';
import BackToTop from './components/BackToTop.vue';

</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar/>
    <HeroSection/>
    <ServiceSection/>
    <AboutSection/>
    <ExperienceAndSkills/>
    <LatestProjSection/>
    <ContactSection/>
    <TestimonialsSection/>
    <FooterSection/>
    <BackToTop/>
  </div>
</template>
