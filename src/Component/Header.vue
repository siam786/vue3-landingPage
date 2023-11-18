<template>
  <nav class="sticky top-0 z-50 w-full bg-gray-300 border-b">
    <div
      class="container flex items-center justify-between px-6 py-5 mx-auto md:py-0"
    >
      <div aria-label="Home. logo" role="img">
        <img  class="w-12 md:w-auto" src="../assets/logo.png" alt="logo" />
      </div>
      <div>
        <button
          @click="toggleMenu(false)"
          class="text-white sm:block md:hidden hover:text-gray-300 focus:text-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-500"
        >
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
</svg>

        </button>
        <div id="menu" class="hidden md:block lg:block">
          <button
            
            class="fixed top-0 z-30 block mt-6 text-gray-500 md:hidden lg:hidden hover:text-gray-700 focus:text-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-500"
          >
            <svg
              aria-label="close main menu"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="#2c3e50"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path stroke="none" d="M0 0h24v24H0z" />
              <line x1="18" y1="6" x2="6" y2="18" />
              <line x1="6" y1="6" x2="18" y2="18" />
            </svg>
          </button>
          <ul
            class="fixed top-0 bottom-0 left-0 right-0 z-20 flex flex-col items-center justify-center py-10 text-3xl bg-white md:text-base md:flex md:flex-row md:relative md:bg-transparent"
          >
            <li
              v-for="(menuItem, index) in menuItems"
              :key="index"
              class="pt-10 text-base cursor-pointer hover:text-gray-900 lg:text-lg md:pt-0 md:ml-5 lg:ml-10"
            >
              <a class="font-semibold" :href="menuItem.link">{{
                menuItem.label
              }}</a>
            </li>
          </ul>
        </div>
      </div>
      <button
        class="hidden px-4 py-1 text-sm text-indigo-700 transition duration-150 ease-in-out bg-transparent border border-indigo-700 rounded focus:outline-none lg:text-lg lg:font-bold focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 md:block hover:bg-gray-200 sm:px-8 sm:py-3"
      >
        Sign In
      </button>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const menuItems = [
  { label: "Hero", link: "#hero" },
  { label: "Features", link: "#features" },
  { label: "Call To Action", link: "#cta" },
  // Add more menu items as needed
];
const isMobileMenuOpen = ref(false);
const toggleMenu = (open) => {
  isMobileMenuOpen.value = open;
};
</script>

<style></style>
