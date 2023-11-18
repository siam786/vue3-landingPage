<template>
    <section id="features" class="pt-20 lg:pt-[120px] pb-12 lg:pb-[90px]">
      <div class="container mx-auto">
        <div class="flex flex-wrap -mx-4">
          <div class="w-full px-4">
            <div class="text-center mx-auto mb-12 lg:mb-20 max-w-[510px]">
              <span class="block mb-2 text-lg font-semibold text-primary">
                Our Services
              </span>
              <h2 class="font-bold text-3xl sm:text-4xl md:text-[40px] text-dark mb-4">
                What We Offer
              </h2>
              <p class="text-base text-body-color">
                There are many variations of passages of Lorem Ipsum available but the majority have suffered alteration in some form.
              </p>
            </div>
          </div>
        </div>
  
        <div class="flex flex-wrap -mx-4">
          <div v-for="(service, index) in services" :key="index" class="w-full px-4 md:w-1/2 lg:w-1/3">
            <div class="p-10 md:px-7 xl:px-10 rounded-[20px] bg-[#3056d3] text-white shadow-md hover:shadow-lg mb-8">
              <div class="w-[70px] h-[70px] flex items-center justify-center">
                <!-- Dynamically load SVG icon -->
                <div v-html="service.icon"></div>
              </div>
              <h4 class="mb-3 text-xl font-semibold">{{ service.title }}</h4>
              <p>{{ service.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const services = ref([
    {
      title: 'Computer Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" d="M13 5l7 7-7 7M5 5l7 7-7 7"/>
        </svg>
      `
    },
    {
      title: 'Laptop Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <rect width="20" height="14" x="2" y="6" rx="2" ry="2"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M8 21h8"/>
        </svg>
      `
    },
    {
      title: 'Mouse Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" d="M8 16l-2.5 1.5a7.7 7.7 0 0 0-3.8 6.6V20a1 1 0 0 0 1 1h20a1 1 0 0 0 1-1v-1.9a7.7 7.7 0 0 0-3.8-6.6L16 16"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M2 12l3.5 2a7.7 7.7 0 0 0 3.8 0L22 12M2 12l3.5-2a7.7 7.7 0 0 1 3.8 0l12.7 7.3"/>
        </svg>
      `
    },
    {
      title: 'Camera Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <circle cx="12" cy="12" r="3"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M17 11h2a4 4 0 0 1-8 0h2"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M12 2a9 9 0 0 1 9 9a4 4 0 0 1-4 4"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M3 13a9 9 0 0 1 9-9a4 4 0 0 1 4 4"/>
          <path stroke-linecap="round" stroke-linejoin="round" d="M8 21h8"/>
        </svg>
      `
    },
    {
      title: 'Phone Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" d="M22 15l-4-4-4 4m4-4V4h-4v7M2 18h16v4H2v-4z"/>
        </svg>
      `
    },
    {
      title: 'Headphone Service',
      description: 'We enjoy working with discerning clients, people for whom quality, service, integrity & aesthetics.',
      icon: `
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" width="40" height="40" stroke-width="1.5" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" d="M8 9l4-4 4 4m0 6v5a3 3 0 0 1-3 3H6a3 3 0 0 1-3-3v-5m0 0a5 5 0 0 1 10 0"/>
        </svg>
      `
    },
  ]);
  
  </script>
  
  <style>
  /* Your styles here */
  </style>
  