<script setup>
import {ref} from 'vue';
import {Carousel , Navigation , Slide} from 'vue3-carousel';
import 'vue3-carousel/carousel.css'

// carousel setting
const settings= ref({
    itemsToShow:3,
    snapAlign:"center",
})
// BreakPoints
const breakpoints= ref({
    
    1024:{
        itemsToShow:3,
        snapAlign:'start',
    },
    768:{
        itemsToShow:2,
        snapAlign:'center',
    },
    480:{
        itemsToShow:1,
        snapAlign:'center',
    },
})

const testimonials= ref([
    {
        id:1,
        FullName:'Client 1',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },
    {
        id:2,
        FullName:'Client 2',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },{
        id:3,
        FullName:'Client 3',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },{
        id:4,
        FullName:'Client 4',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },{
        id:5,
        FullName:'Client 5',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },{
        id:6,
        FullName:'Client 6',
        image:'/src/assets/As-26.png',
        commit:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod'
    },
])
</script>


<template>
    <section class="text-white mt-20" id="testimonials" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Testimonials</h2>
        <div class="px-4 xl:pl-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints">
                <Slide v-for="element in testimonials" :key="element.id">
                    <div class="carousel__item p-4">
                        <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5 text-white font-light mb-6">
                             <div class="w-full flex mb-4 items-center">
                                <div class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200">
                                    <img :src="element.image" alt="testimonials image" loading="lazy">
                                </div>
                                <h6 class="ml-4 font-bold text-sm uppercase text-white">{{ element.FullName }}</h6>
                             </div>
                             <div class="w-full">
                                <p class="text-sm leading-tight">
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                    {{ element.commit }}
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                </p>
                             </div>
                        </div>
                    </div>
                </Slide>
                <template #addons>
                    <Navigation/>
                </template>
            </Carousel>
        </div>
    </section>
</template>

<style>
.carousel__prev,.carousel__next{
    color: white !important;
}
</style>