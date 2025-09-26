<script setup>
import { reactive, ref } from 'vue'

const showAll = ref(false)

const states = reactive([
  {
    img: '/images/dart.png',
    title: 'dart',
    subtitle: 'A modern, object-oriented programming language',
    subtitle1: 'Modern OOP language',
  },
  {
    img: '/images/flutter.png',
    title: 'flutter',
    subtitle: 'UI toolkit for creating natively compiled mobile, web, and desktop app',
    subtitle1: 'UI toolkit for cross-platform apps',
  },
  {
    img: '/images/java.png',
    title: 'java',
    subtitle: 'object-oriented programming language widely used backend development.',
    subtitle1: 'used language for backend',
  },
  {
    img: '/images/getx.png',
    title: 'getx',
    subtitle: 'Lightweight Flutter state management, navigation',
    subtitle1: 'Lightweight state management',
  },
  {
    img: '/images/jj.png',
    title: 'provider',
    subtitle: 'Popular Flutter state management library for scalable app architecture',
    subtitle1: 'Scalable state management library',
  },
  {
    img: '/images/restapi.png',
    title: 'Rest api',
    subtitle: 'A standard architecture for seamless client-server communication',
    subtitle1: 'Standard client-server communication',
  },
  {
    img: '/images/mvvc.png',
    title: 'mvvm',
    subtitle: 'Software design pattern separating UI, logic, and data handling for cleaner apps',
    subtitle1: 'Clean separation of UI, logic & data',
  },
  {
    img: '/images/mvc.png',
    title: 'mvc',
    subtitle: 'Classic software architecture dividing model, view, and controller layers',
    subtitle1: 'Model, View & Controller pattern',
  },
  // read more state
  {
    img: '/images/oop.png',
    title: 'oop',
    subtitle: 'Object-Oriented Programming paradigm for modular reusable',
    subtitle1: 'Modular, reusable coding approach',
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
    subtitle: 'Google’s mobile advertising platform for app monetization',
    subtitle1: 'Mobile app monetization tool',
  },
  {
    img: '/images/map.png',
    title: 'google map',
    subtitle: 'Location and navigation API for integrating maps in mobile apps',
    subtitle1: 'Location & navigation API'
  },
  {
    img: '/images/eps.png',
    title: 'eps',
    subtitle: 'Electronic Payment System for secure online transactions',
    subtitle1: 'Secure electronic payment system'
  },
  {
    img: '/images/SSLCOMMERZ.png',
    title: 'SSLCOMMERZ',
    subtitle: 'Bangladesh’s leading online payment gateway for e-commerce and apps',
    subtitle1: 'Leading BD online payment gateway'
  },
  {
    img: '/images/git.png',
    title: 'git',
    subtitle: 'Version control system for tracking and managing code changes',
    subtitle1: 'Version control system'
  },
  {
    img: '/images/github.png',
    title: 'github',
    subtitle: 'Cloud-based Git repository hosting and collaboration platform',
    subtitle1: 'Cloud Git repository platform'
  },
  {
    img: '/images/figma.png',
    title: 'figma',
    subtitle: 'Online collaborative tool for UI/UX design and prototyping',
    subtitle1: 'Collaborative UI/UX design tool'
  },
  {
    img: '/images/jira.png',
    title: 'jira',
    subtitle: 'Project management and issue tracking tool for Agile teams',
    subtitle1: 'Agile project management tool'
  },
  {
    img: '/images/postman.png',
    title: 'postman',
    subtitle: 'API development, testing, and collaboration platform',
    subtitle1: 'API testing & development tool',
  },
  {
    img: '/images/trello.png',
    title: 'trello',
    subtitle: 'Visual project management tool with boards, lists, and cards',
    subtitle1: 'Visual project management board'
  },
])
</script>

<template>
<section id="skill">
  <section class="py-8 items-center">
    <section class="text-center">
      <h1 class="lg:text-2xl xs:text-xl font-serif font-bold xs:mt-2 md:mt-2 lg:-mt-5">
        <span class="text-cyan-400">My Skills</span>
      </h1>
      <p class="mt-2 text-white">Technologies I work with</p>
      <div class="w-20 lg:h-1 xs:h-0.5 bg-cyan-500 mx-auto mt-3 rounded"></div>
    </section>

    <section class="w-full xs:mt-8 lg:mt-16 px-3 md:px-12 grid lg:gap-4 md:gap-4 xs:gap-2 xs:grid-cols-2 md:grid-cols-2 lg:grid-cols-4">
      <div
        v-for="(state, index) in states"
        :key="index"
        v-show="showAll || index < 8"
        class="w-full lg:w-full md:w-full xs:w-full h-auto xs:h-[144px] md:h-[200px] p-3 rounded-lg bg-gray-900 dark:border-gray-700 transition-transform duration-500 
               xs:border lg:dark:border-2 border-cyan-700 hover:border-2 hover:border-cyan-400 hover:scale-[1.03] sm:w-[30px] lg:h-[210px] xs:p-3 md:p-5 hover:shadow-lg shadow"
      >
        <div class="bg-gray-300 p-3 rounded-full flex text-blue-600 lg:w-14 lg:h-14 xs:w-11 xs:h-11 justify-center items-center">
          <img class="lg:w-[30px] lg:h-[30px] xs:w-[26px] xs:h-[18px]" :src="state.img" alt="" />
        </div>
        <div class="">
          <h1 class="xs:text-[13.5px] md:text-lg text-cyan-400 uppercase font-bold mt-4">{{ state.title }}</h1>
          <p class="hidden md:block lg:text-base mb-3 md:mt-3 lg:mt-2 font-normal text-cyan-200 dark:text-cyan-300">
            {{ state.subtitle }}
          </p>
          <p class="block lg:hidden md:hidden xs:text-[12px] md:text-xl lg:text-xl mb-3 md:mt-3 lg:mt-4 font-normal text-cyan-200 dark:text-cyan-300">
            {{ state.subtitle1 }}
          </p>
        </div>
      </div>
    </section>

    <!-- Read More / Read Less Button -->
    <div class="text-center mt-8">
      <button
        @click="showAll = !showAll"
        class="py-2 px-6 text-sm font-medium text-black bg-cyan-400 border border-cyan-400 rounded-full shadow-md hover:bg-[#1f242d] hover:text-white transition"
      >
        {{ showAll ? 'Show Less' : 'Read More' }}
      </button>
    </div>
  </section>
</section>
</template>
