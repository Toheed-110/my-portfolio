<script setup>
import { ref } from 'vue';
const education =ref([
    {
        id:1,
        school:'Lahore Garrison University',
        program:'Software Engineering',
        year:'2019-2023'
    },
    {
        id:2,
        school:'The Educator School Shakargarh',
        program:'Intermediate',
        year:'2019'
    },
    {
        id:3,
        school:'Govt. Higher Secondary School Kot Nainan',
        program:'Matric',
        year:'2016'
    },

]);
</script>


<template>
    <section class="text-white mt-18" id="about">
        <!-- <div class="absolute z-0 top-[93rem] insert-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-[#FB7E09] via-[#D3295D] to-[#570cac] opacity-20"></div>
        </div> -->
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl text-white text-left mb-8"> My Education</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
                        <div class="w-1/4">
                            <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap--v1">
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#FB7E09] to-[#D3295D] lg:text-xl">
                                {{ element.school }}
                            </h3>
                            <p class="text-white">{{ element.program }}</p>
                            <p class="text-white">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">More
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#FB7E09] to-[#D3295D]">About</span>
                     Me
                </h2>
                <p class="text-base lg:text-lg mt-8 py-8">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam quisquam quos rem animi
                     pariatur quidem perferendis enim doloribus earum eligendi impedit culpa est qui assumenda iste ex placeat, natus omnis?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam quisquam quos rem animi
                     pariatur quidem perferendis enim doloribus earum eligendi impedit culpa est qui assumenda iste ex placeat, natus omnis?
                </p>
                <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+200</h3>
                        <p class="text-sm sm:text-base text-gray-300">Happy Client</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+100</h3>
                        <p class="text-sm sm:text-base text-gray-300">Projects</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+5</h3>
                        <p class="text-sm sm:text-base text-gray-300">Years Experience</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


