<script setup>
import { ref,computed } from 'vue';


const Projects =ref([
  {
    id:1,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 1',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
  {
    id:2,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 2',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
  {
    id:3,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 3',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
  {
    id:4,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 4',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
  {
    id:5,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 5',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
  {
    id:6,
    category:'Web Development',
    image:'/src/assets/toheed.png',
    title:'project 6',
    description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident animi eligendi quaerat magnam dolor voluptatem, neque harum doloremque. Error unde quos tempore. Nemo fugiat deserunt, nesciunt distinctio doloremque vel sunt.',
    technologies:['vue Js','node Js'],
    gitURL:'',
    webURL:'',
  },
])

const selectedCategory = ref('All');
const filteredProjects =computed(()=>{
  if(selectedCategory.value === 'All'){
     return Projects.value;
  }
  return Projects.value.filter(project=>project.category.toLocaleLowerCase()=== selectedCategory.value.toLocaleLowerCase());
})
</script>



<template>
    <section class="text-white mt-20">
        <div class="px-4 xl:pl-16">
            <div class="mb-4 md:flex md:justify-between xl:pr-26">
                <h2 class="text-4xl font-bold text-white">My Latest Projects</h2>
                <div class="flex space-x-4 mb-4 mt-5 md:nt-0">
                    <button class="hover:text-[#FB7E09]" v-for="category in ['All','Web Development','App Development']"
                    :key="category" @click="(()=>selectedCategory = category)">
                    {{ category }}
                   </button>
                </div>
            </div>
            <!-- <div v-for="project in filteredProjects" :key="project.id" class="border border-gray-400 bg-gray-800 w-full rounded-xl flex flex-col items-center gap-y-4">
                  <img :src="project.image" alt="image" class="w-full">
                  <h1>{{  project.title }}</h1>
                  <p>{{  project.description }}</p>
                </div> -->
            <ul class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3" data-aos="fade-right">
              <div v-for="project in filteredProjects" :key="project.id" class="border border-gray-400 bg-gray-800 w-full rounded-xl flex flex-col items-center gap-y-4">
                  <img :src="project.image" alt="image" class="w-full">
                  <h1>{{  project.title }}</h1>
                  <p>{{  project.description }}</p>
                </div>
                <!-- <div v-for="project in filteredProjects" :key="project.id">
                  <div class="h-52 md:h-[24rem] rounded-t-xl relative gruop"
                  :style="{backgroundImage:'url('+project.image+')',backgroundSize:'cover'}">
                  <div class="overlay items-center justify-center absolute top-0 left-0 w-full h-full bg-[#181818] bg-opacity-0
                  hidden group-hover:flex group-hover:bg-opacity-80 transition-all duration-500"
                  >
                  <a class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                    :href="project.webURL"> <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                      viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true"
                      data-slot="icon"
                      class="h-10 w-10 text-[#AD87BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer">
                      <path stroke-linecap="round" stroke-linejoin="round"
                         d="M17.25 6.75 22.5 121-5.25 5.25m-10.5 011.5 1215.25-5.25m7.5-3-4.5 16.5">
                      </path>
                      </svg>
                  </a>
                  <a class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                    :href="project.webURL"> <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                      viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true"
                      data-slot="icon"
                      class="h-10 w-10 text-[#AD87BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer">
                      <path stroke-linecap="round" stroke-linejoin="round"
                          d="M17.25 6.75 22.5 121-5.25 5.25m-10.5 011.5 1215.25-5.25m7.5-3-4.5 16.5">
                      </path>
                      <path stroke-linecap="round" stroke-linejoin="round"
                        d="M15 1223 3 011-60330016 0Z">
                      </path>
                      </svg>
                  </a>

                  </div>
                  </div>
                </div> -->
            </ul>
            
        </div>
    </section>
</template>




