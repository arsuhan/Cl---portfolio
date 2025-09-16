<script setup>
import { reactive, ref } from 'vue'

const open = ref(true)
const states = reactive([
  {
    img: '/images/dart.png',
    title: 'dart',
    subtitle: 'Semantic markup, accessibility standards, SEO optimization',
    subtitle1: 'Semantic tags, SEO, a11y',
  },
  {
    img: '/images/flutter.png',
    title: 'flutter',
    subtitle: 'Responsive design, animations, Flexbox/Grid layouts',
     subtitle1: 'Alignment Structure Motion Grid',
  },
  {
    img: '/images/java.png',
    title: 'java',
    subtitle: 'Modern UI design with bootstrap 5 design with',
    subtitle1: 'Bootstrap 5 UI Design',
  },
  {
    img: '/images/getx.png',
    title: 'getx',
    subtitle: 'ES6+, DOM manipulation, async programming',
    subtitle1: 'ES6, DOM, Async /Await',
  },
  {
    img: '/images/jj.png',
    title: 'provider',
    subtitle: 'Designing Custom Layouts with Tailwind CSS',
    subtitle1: 'Utility-first Layouts',
  },
  {
    img: '/images/restapi.png',
    title: 'Rest api',
    subtitle: 'Frontend Web Development using Vue.js',
    subtitle1: 'Vue 3, Components, Props',
  },
  {
    img: '/images/mvvc.png',
    title: 'mvvc',
    subtitle: 'Interactive UI Elements with Flowbite,',
    subtitle1: 'UI Kit + Tailwind CSS',
  },
  {
    img: '/images/mvc.png',
    title: 'mvc',
    subtitle: 'Data Storage and Retrieval using MongoDB',
    subtitle1: 'NoSQL, CRUD, Atlas DB',
  },
   {
    img: '/images/firebase.png',
    title: 'firebase',
    subtitle: 'Building Real-Time Applications with Firebase',
    subtitle1: 'Auth, DB, Hosting',
  },
  {
    img: '/images/admod.png',
    title: 'AdMob',
    subtitle: 'Deploy Stunning Websites on Netlify',
    subtitle1: 'Deploy Stunning Websites on Netlify',
  },
  {
    img: '/images/map.png',
    title: 'google map',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/eps.png',
    title: 'eps',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/SSLCOMMERZ.png',
    title: 'SSLCOMMERZ',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/git.png',
    title: 'git',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/github.png',
    title: 'github',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/figma.png',
    title: 'figma',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/jira.png',
    title: 'jira',
    subtitle: 'Version control, GitHub, CI/CD workflows',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/postman.png',
    title: 'postman',
    subtitle: 'Test and Debug APIs Effortlessly',
    subtitle1: 'Test and Debug APIs Effortlessly',
  },
  {
    img: '/images/trello.png',
    title: 'trello',
    subtitle: 'Visual project management tool with boards, lists, and cards.',
    subtitle1: 'Git, Commits, CI/CD'
  },
  {
    img: '/images/oop.png',
    title: 'oop',
    subtitle: 'Object-Oriented Programming paradigm for modular, reusable, and maintainable code.',
    subtitle1: 'UI Kit + Tailwind CSS',
  },
])

</script>

<template>
    <section id="skill" class="">
  <section class="py-8 -my-1 items-center">
    <section class="text-center">
      <h1 class="lg:text-3xl xs:text-xl font-serif font-bold xs:mt-2 md:mt-2 lg:-mt-5">
        <span class="text-white">My </span>
        <span class="text-cyan-400">Skills</span>
      </h1>
      <p class="mt-2 lg:text-[20px] text-white">Technologies I work with</p>
      <div class="w-20 lg:h-1 xs:h-0.5 bg-cyan-500 mx-auto mt-3 rounded"></div>
    </section>

    <section
     
      class="w-full xs:mt-8 lg:mt-16 px-3 md:px-12 grid lg:gap-4 md:gap-4 xs:gap-2 xs:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 "
    >

      <div v-for="state in states"
     
     class="w-full lg:w-full md:w-full xs:w-full h-auto xs:h-[144px] md:h-[200px] p-3 lg:p-6 rounded-lg bg-gray-900 dark:border-gray-700 transition-transform duration-500 
      xs:border lg:dark:border-2 border-cyan-700 hover:border-2 hover:border-cyan-400 hover:scale-[1.03] sm:w-[30px] lg:h-[220px] xs:p-3 md:p-5 hover:shadow-lg shadow"
>
      
        <div class="bg-gray-300 p-3 rounded-full flex text-blue-600 lg:w-14 lg:h-14 xs:w-11 xs:h-11 justify-center items-center">
                  <img class="lg:w-[30px] lg:h-[30px] xs:w-[26px] xs:h-[18px]" :src="state.img" alt="" />
        </div>
        <div class="">
          <h1 class="lg:text-xl xs:text-[13.5px] md:text-lg text-cyan-400 uppercase font-bold mt-4">
          {{ state.title }}
        </h1>
        <p class="hidden md:block md:text-xl lg:text-[17px] md:text-[14px] mb-3 md:mt-3 lg:mt-2 font-normal text-cyan-200 dark:text-cyan-300">
          {{ state.subtitle }}
        </p>
        <p class="block lg:hidden md:hidden xs:text-[13px] md:text-xl lg:text-xl mb-3 md:mt-3 lg:mt-4 font-normal text-cyan-200 dark:text-cyan-300 mt-1">
          {{ state.subtitle1 }}
        </p>
        </div>
      </div>
    </section>
  </section>
</section>
</template>