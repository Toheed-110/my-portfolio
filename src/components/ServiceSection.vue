<script setup>
 import { ref } from 'vue';
 const services =ref([
    {
        id:1,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/web-design.png',
        name:'WEB DEVELOPMENT',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque aliaLorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
    {
        id:2,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name:'APP DEVELOPMENT',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
    {
        id:3,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/google-code.png',
        name:'TECHNICAL WRITING',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
    {
        id:4,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/google-code.png',
        name:'DIGITAL MARKETING',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
    {
        id:5,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/email-open.png',
        name:'CONTENT WRITING',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
    {
        id:6,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name:'GRAPHIC DESINING  ',
        discription:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque alia',
    },
 ])

</script>

<template>
  <section class="text-white mt-20" id="services">
    <div class="px-4 xl:pl-16">
        <h2 class="text-4xl text-white mb-4 font-bold">My Services</h2>
    </div>
    <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
        <div v-for="service in services" :key="service.id" data-aos="fade-up"
        class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] flex flex-col items-center">
            <div class="h-24 xl:h-28 xl:w-28">
                <img :src="service.icon" alt="service icon">
            </div>
             <div>
                <h3 class="text-center pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#FB7E09] to-[#D3295D] lg:text-xl">
                    {{ service.name }}
                </h3>
                <p class="pt-4 text-center text-gray-400 text-sm group-hover:text-white md:text-base">
                    {{ service.discription }}
                </p>
             </div>
        </div>
    </div>

  </section>
</template>

