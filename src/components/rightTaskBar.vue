<script setup>
</script>

<template>
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
</template>

<style scoped>
</style>
