
<script setup>
import { ref, computed } from 'vue';

// Projects list
const Projects = ref([
  {
    id: 1,
    category: 'Web Development',
    image: '/src/assets/toheed.png', // Or use `require('@/assets/toheed.png')` if needed
    title: 'Project 1',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project1',
    webURL: 'https://example.com/project1',
  },
  {
    id: 2,
    category: 'Web Development',
    image: '/src/assets/toheed.png',
    title: 'Project 2',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project2',
    webURL: 'https://example.com/project2',
  },
  {
    id: 3,
    category: 'Web Development',
    image: '/src/assets/toheed.png',
    title: 'Project 3',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project2',
    webURL: 'https://example.com/project2',
  },
  {
    id: 4,
    category: 'Web Development',
    image: '/src/assets/toheed.png',
    title: 'Project 4',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project2',
    webURL: 'https://example.com/project2',
  },
  {
    id: 5,
    category: 'Web Development',
    image: '/src/assets/toheed.png',
    title: 'Project 5',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project2',
    webURL: 'https://example.com/project2',
  },
  {
    id: 6,
    category: 'Web Development',
    image: '/src/assets/toheed.png',
    title: 'Project 6',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quonatus distinctio voluptate ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam,tenetur! Nihil quoderror labore nam doloribus.',
    technologies: ['Vue.js', 'Node.js'],
    gitURL: 'https://github.com/example/project2',
    webURL: 'https://example.com/project2',
  },
  // ... more projects
]);

// Filtering logic
const selectedCategory = ref('All');
const filteredProjects = computed(() => {
  if (selectedCategory.value === 'All') {
    return Projects.value;
  }
  return Projects.value.filter(
    (project) =>
      project.category.toLowerCase() === selectedCategory.value.toLowerCase()
  );
});
</script>

<template>
  <section class="text-white mt-20">
    <div class="px-4 xl:pl-16">
      <div class="mb-4 md:flex md:justify-between xl:pr-26">
        <h2 class="text-4xl font-bold">My Latest Projects</h2>
        <div class="flex space-x-4 mb-4 mt-5 md:mt-0">
          <button
            v-for="category in ['All', 'Web Development', 'App Development']"
            :key="category"
            @click="selectedCategory = category"
            class="hover:text-[#FB7E09]"
          >
            {{ category }}
          </button>
        </div>
      </div>

      <ul
        class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
        data-aos="fade-right"
      >
        <li
          v-for="project in filteredProjects"
          :key="project.id"
          class="border border-gray-400 bg-gray-800 w-full rounded-xl flex flex-col items-center gap-y-4"
        >
          <div
            class="h-52 md:h-[24rem] rounded-t-xl relative group w-full"
            :style="{ backgroundImage: 'url(' + project.image + ')', backgroundSize: 'cover', backgroundPosition: 'center' }"
          >
            <div
              class="overlay items-center justify-center absolute top-0 left-0 w-full h-full bg-[#181818] bg-opacity-0 hidden group-hover:flex group-hover:bg-opacity-80 transition-all duration-500"
            >
              <!-- Live site button -->
              <a
                :href="project.webURL"
                target="_blank"
                class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="h-10 w-10 text-[#AD87BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M13.5 4.5L19.5 10.5M13.5 4.5H16.5M13.5 4.5V7.5M6 9V15H12V9H6Z"
                  />
                </svg>
              </a>

              <!-- GitHub button -->
              <a
                :href="project.gitURL"
                target="_blank"
                class="h-14 w-14 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                  class="h-10 w-10 text-[#AD87BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer"
                >
                  <path
                    d="M12 0C5.371 0 0 5.371 0 12a12.01 12.01 0 008.208 11.385c.6.111.82-.26.82-.577v-2.17c-3.338.726-4.042-1.613-4.042-1.613-.546-1.387-1.334-1.756-1.334-1.756-1.09-.745.083-.729.083-.729 1.205.084 1.84 1.237 1.84 1.237 1.07 1.835 2.809 1.305 3.495.997.108-.775.419-1.305.763-1.605-2.665-.303-5.466-1.332-5.466-5.931 0-1.31.469-2.382 1.236-3.221-.124-.303-.536-1.52.117-3.167 0 0 1.008-.322 3.3 1.23a11.51 11.51 0 016.003 0c2.29-1.552 3.296-1.23 3.296-1.23.655 1.647.243 2.864.12 3.167.77.84 1.234 1.911 1.234 3.221 0 4.61-2.805 5.624-5.475 5.921.43.371.823 1.102.823 2.222v3.293c0 .32.218.694.825.576A12.011 12.011 0 0024 12c0-6.629-5.371-12-12-12z"
                  />
                </svg>
              </a>
            </div>
          </div>
          <div class="p-4 text-center">
            <h3 class="text-xl font-bold">{{ project.title }}</h3>
            <p class="text-sm text-justify  mt-2">{{ project.description }}</p>
            <p class="text-xs text-gray-400 mt-2">
              {{ project.technologies.join(', ') }}
            </p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>




