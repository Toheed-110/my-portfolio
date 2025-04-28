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
        program:'Inter',
        year:'2019'
    },
    

]);
</script>


<template>
    <section class="text-white mt-18" id="about">
        <div class="absolute z-0 top-[93rem] insert-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-[#FB7E09] via-[#D3295D] to-[#570cac] opacity-20"></div>
        </div>
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
        </div>
    </section>
</template>


<style>
</style>