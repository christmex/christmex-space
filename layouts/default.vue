<script setup>
  import { SpeedInsights } from '@vercel/speed-insights/vue';
</script>


<template>
  <SpeedInsights />
  <ul class="circles">
      <li></li><li></li><li></li><li></li><li></li><li></li><li></li><li></li><li></li><li></li><li></li>
  </ul>
  <!-- <div class="absolute -z-10 inset-0 bg-[url(/img/grid.svg)] -top-10 [mask-image:linear-gradient(180deg,white,rgba(255,255,255,0))]"></div> -->
  
  <div class="container p-4 mx-auto sm:w-[1080px]">
    <header class="flex justify-between py-4">
        <div class="brand">
          <h1 class="font-bold text-xl"><NuxtLink to="/">👻 Jonathan Christian</NuxtLink></h1>
          <span class="text-sm italic">Building apps by day, hunting bugs by night.</span>
        </div>
        <nav>
        <ul class="md:flex space-x-8 hidden">
            <!-- <li class="font-medium text-red"><NuxtLink to="/" activeClass="text-green-600">Home</NuxtLink></li> -->
            <!-- <li class="font-medium text-red"><NuxtLink to="/about" activeClass="text-green-600">About</NuxtLink></li> -->
            <!-- <li class="font-medium"><NuxtLink to="" activeClass="text-green-600">Portofolio</NuxtLink></li> -->
            <li class="font-medium"><a href="mailto:christmex@wearehackerone.com" class="text-green-600">💸 Hire Me</a></li>
            <li class="font-medium"><NuxtLink to="https://christmex.medium.com/" target="_blank" activeClass="text-green-600">Blogs</NuxtLink></li>
            <li class="font-medium">
              <a href="https://github.com/christmex/" class="" target="_blank">
                <img src="/img/github-mark.svg" alt="" class="size-6">
              </a>
            </li>
        </ul>
        <div class="md:hidden">
          <button @click="toggleClass" data-ripple-light="true" data-popover-target="menu"
            class="select-none py-3 px-6 text-center align-middle font-sans text-xs font-bold uppercase transition-all focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] active:shadow-none disabled:pointer-events-none disabled:opacity-50 disabled:shadow-none">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
          </button>
          <ul role="menu" data-popover="menu" data-popover-placement="bottom"
            class="absolute z-10 min-w-[180px] right-4 overflow-auto rounded-md border border-blue-gray-50 bg-white p-3 font-sans text-sm font-normal text-blue-gray-500 shadow-lg shadow-blue-gray-500/10 focus:outline-none
            " :class="{ 'hidden': isActive }">
            <!-- <li role="menuitem"
              class="block w-full cursor-pointer select-none rounded-md px-3 pt-[9px] pb-2 text-start leading-tight transition-all hover:bg-blue-gray-50 hover:bg-opacity-80 hover:text-blue-gray-900 focus:bg-blue-gray-50 focus:bg-opacity-80 focus:text-blue-gray-900 active:bg-blue-gray-50 active:bg-opacity-80 active:text-blue-gray-900">
              <NuxtLink to="/" activeClass="text-green-600">Home</NuxtLink>
            </li> -->
            <li role="menuitem"
              class="block w-full cursor-pointer select-none rounded-md px-3 pt-[9px] pb-2 text-start leading-tight transition-all hover:bg-blue-gray-50 hover:bg-opacity-80 hover:text-blue-gray-900 focus:bg-blue-gray-50 focus:bg-opacity-80 focus:text-blue-gray-900 active:bg-blue-gray-50 active:bg-opacity-80 active:text-blue-gray-900">
              <a href="mailto:christmex@wearehackerone.com" class="">Hire Me</a>
            </li>
            <li role="menuitem"
              class="block w-full cursor-pointer select-none rounded-md px-3 pt-[9px] pb-2 text-start leading-tight transition-all hover:bg-blue-gray-50 hover:bg-opacity-80 hover:text-blue-gray-900 focus:bg-blue-gray-50 focus:bg-opacity-80 focus:text-blue-gray-900 active:bg-blue-gray-50 active:bg-opacity-80 active:text-blue-gray-900">
              <NuxtLink to="https://christmex.medium.com/" target="_blank" activeClass="text-green-600">Blogs</NuxtLink>
            </li>
            <li role="menuitem"
              class="block w-full cursor-pointer select-none rounded-md px-3 pt-[9px] pb-2 text-start leading-tight transition-all hover:bg-blue-gray-50 hover:bg-opacity-80 hover:text-blue-gray-900 focus:bg-blue-gray-50 focus:bg-opacity-80 focus:text-blue-gray-900 active:bg-blue-gray-50 active:bg-opacity-80 active:text-blue-gray-900">
              <a href="https://github.com/christmex/" class="">Github
              </a>
            </li>
          </ul>
        </div>
        </nav>
    </header>
    <div>
      <div class="mt-4 md:mt-6 2xl:mt-10">
        <div class="mx-auto grid max-w-2xl grid-cols-1 items-center gap-x-8 gap-y-16 lg:max-w-7xl lg:grid-cols-2">
        <div>
            <img src="/img/hero.svg" alt="" class="rounded-full md:w-3/5">
            <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">TALL Dev &<br> IT Security Enthusiast</h2>
            <p class="mt-4 text-gray-500">
                Hey there! I'm Jonathan from Indonesia.
                Over the past few years, I've been busy building applications. In between, I carve out time to write articles about cybersecurity and participate in bug bounty programs.

                <!-- Learn things about technology, such as Cyber Security,<br>Web Technology and UI/UX design. -->
            </p>
            <a href="mailto:christmex@wearehackerone.com" class="px-4 inline-block bg-green-600 text-white font-medium p-2 rounded-md mt-6">💸 Hire Me</a>
            
        </div>
        <slot />
        </div>
    </div>
    </div>
    <footer class="mx-auto mt-8 w-full max-w-container px-4 sm:px-6 lg:px-8">
    <div class="border-t border-slate-900/5 py-6">
        <p class="text-center text-sm leading-6 text-slate-500">©
            <!-- -->2024<!-- -->
            Made with ❤️ by me. All rights reserved.</p>
    </div>
</footer>
  </div>
</template>

<script>

export default {
    data() {
      return {
        isActive: true // Menyimpan status kelas
      };
    },
    methods: {
      toggleClass(event) {
        this.isActive = !this.isActive; // Mengubah status kelas saat tombol diklik
      },
      setActive(){
        this.isActive = true;
      }
    }
  };
</script>