<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
   <div class="container min-w-full min-h-screen">
    
    <div class="taskBar absolute bottom-0 w-full min-w-[854px] py-0  bg-slate-900 flex-row inline-flex justify-between place-items-center">
        <div class="w-36  mx-1 px-2 py-1 flex flex-row space-x-2 justify-start place-items-center rounded-[4px] hover:bg-slate-700">
         <img src="./assets/icons/weather/003-cloudy.png" alt="weatherIcon" class="h-7">
         <div class="text-xs text-zinc-100 font-semibold font-mono">
          <p>24<sup>o</sup>C</p>
          <p>Cloudy</p>
         </div>

        </div>
        <div class="max-w-max -mr-[5%] flex flex-row place-items-center">
          <img src="./assets/icons/startIcon.png" class=" hover:bg-slate-700 p-1 rounded-[4px] w-10" alt="Start icon">

          <button class="rounded-full h-8 px-5 mx-1 space-x-2 bg-slate-700 text-slate-50 text-sm font-mono hover:bg-sky-700 active:bg-sky-700 flex align-middle justify-center place-items-center">
            <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
            <p>Search</p>
          </button>

          <img src="./assets/icons/instaIcon.webp" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="insta icon">
          <img src="./assets/icons/storeIcon.png" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="store icon">
          <img src="./assets/icons/taskViewIcon.png" class="hover:bg-slate-700 p-1 rounded-[4px]" width="35px" alt="taskview icon">
          <img src="./assets/icons/notionIcon.png" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="notoin icon">
          <img src="./assets/icons/002-firefox.png" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="firefox icon">
          <img src="./assets/icons/mypcIcon.png" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="mypc icon">
        </div>
        <div class=" w-fit h-12 flex flex-row place-items-center justify-end">
          <button class="uparrow h-full w-fit px-2 text-zinc-50 hover:bg-slate-700">
            <font-awesome-icon icon="fa-solid fa-angle-up" />
          </button>
          <button class="uparrow h-[85%] rounded-[4px] w-fit px-1.5 text-zinc-100 text-xs font-semibold font-sans   hover:bg-slate-700">
            ENG
          </button>
          <button class="text-zinc-100 h-[85%] px-1.5 rounded-[4px] text-sm flex flex-row place-items-center justify-center space-x-1.5 hover:bg-slate-700">    
            <font-awesome-icon icon="fa-solid fa-wifi" />
            <font-awesome-icon icon="fa-solid fa-volume-low" />
            <font-awesome-icon icon="fa-solid fa-battery-empty" class="h-[19px]"/>
           
          </button>
            <div class="date h-[83%] text-xs mx-1.5 px-1.5 rounded-[4px] flex flex-row place-items-center space-x-1.5 text-zinc-100 hover:bg-slate-700">
            <div class="text-zinc-100 text-xs font-mono">
              <p>12:45 PM</p>
              <p>12/16/2022</p>
            </div>
            <font-awesome-icon icon="fa-solid fa-bell" class="text-base"/>
          </div>


        </div>
      </div>

  </div>
</template>

<style scoped>

</style>
