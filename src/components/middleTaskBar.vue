<script setup>


</script>

<template>
  <div class="max-w-max -mr-[5%] flex flex-row place-items-center">
          <img src="../assets/icons/startIcon.png" @click="$emit('toogleStartEvent')"  class=" hover:bg-slate-700 p-1 rounded-[4px] w-10" alt="Start icon">

          <button class="rounded-full h-8 px-5 mx-1 space-x-2 bg-slate-700 text-slate-50 text-sm font-mono hover:bg-sky-700 active:bg-sky-700 flex align-middle justify-center place-items-center">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
</svg>

            <p>Search</p>
          </button>

          <img src="../assets/icons/instaIcon.webp" title="instagram" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="insta icon">
          <img src="../assets/icons/storeIcon.png" title="Microsoft store" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="store icon">
          <img src="../assets/icons/taskViewIcon.png" title="Desktop" class="hover:bg-slate-700 p-1 rounded-[4px]" width="35px" alt="taskview icon">
          <img src="../assets/icons/notionIcon.png" title="Notion" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="notoin icon">
          <img src="../assets/icons/002-firefox.png" title="Firefox" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="firefox icon">
          <img src="../assets/icons/mypcIcon.png" title="My PC" class="hover:bg-slate-700 p-1 rounded-[4px]" width="40px" alt="mypc icon">
        </div>
</template>

<style scoped>
</style>
