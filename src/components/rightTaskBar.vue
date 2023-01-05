<script setup>


var myDate = new Date();

</script>

<template>
  <div class=" w-fit h-12 flex flex-row place-items-center justify-end">
          <button @click="$emit('toogleSmallIconsEvent')" title="Taskbar icons"  class="uparrow h-full w-fit px-1 text-zinc-50 hover:bg-slate-700 outline-none">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 15.75l7.5-7.5 7.5 7.5" />
</svg>

          </button>
          <button title="change input language" class="uparrow h-[85%] rounded-[4px] w-fit px-1.5 text-zinc-100 text-xs font-semibold font-sans   hover:bg-slate-700 outline-none">
            ENG
          </button>
          <button @click="$emit('toogleButtonsEvent')" title="Multiple settings" class="text-zinc-100 h-[85%] px-1.5 rounded-[4px] text-sm flex flex-row place-items-center justify-center space-x-1.5 hover:bg-slate-700 outline-none">    
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M8.288 15.038a5.25 5.25 0 017.424 0M5.106 11.856c3.807-3.808 9.98-3.808 13.788 0M1.924 8.674c5.565-5.565 14.587-5.565 20.152 0M12.53 18.22l-.53.53-.53-.53a.75.75 0 011.06 0z" />
</svg>

<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M19.114 5.636a9 9 0 010 12.728M16.463 8.288a5.25 5.25 0 010 7.424M6.75 8.25l4.72-4.72a.75.75 0 011.28.53v15.88a.75.75 0 01-1.28.53l-4.72-4.72H4.51c-.88 0-1.704-.507-1.938-1.354A9.01 9.01 0 012.25 12c0-.83.112-1.633.322-2.396C2.806 8.756 3.63 8.25 4.51 8.25H6.75z" />
</svg>

<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M21 10.5h.375c.621 0 1.125.504 1.125 1.125v2.25c0 .621-.504 1.125-1.125 1.125H21M3.75 18h15A2.25 2.25 0 0021 15.75v-6a2.25 2.25 0 00-2.25-2.25h-15A2.25 2.25 0 001.5 9.75v6A2.25 2.25 0 003.75 18z" />
</svg>

           
          </button>
            <button @click="$emit('toogleCalendarEvent')" title="Date, time and events" class="date h-[83%] text-xs mx-1.5 px-1.5 rounded-[4px] flex flex-row place-items-center space-x-1.5 text-zinc-100 hover:bg-slate-700 outline-none">
            <div class="text-zinc-100 text-xs font-mono">
              <p>{{ myDate.getHours()}}:{{myDate.getMinutes()}}</p>
              <p>{{ myDate.getMonth()+1}}/{{myDate.getDate()}}/{{myDate.getFullYear()}}</p>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
</svg>

</button>


        </div>
</template>

<style scoped>
</style>
