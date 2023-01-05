<script setup>
import { onBeforeMount, onMounted, ref } from 'vue'



var allProps = defineProps({
  articles: Array,
})






</script>

<template>



<div class="parent rounded-lg mt-3 ml-2 w-[50%] h-[91vh] overflow-hidden transition-opacity duration-700 bg-gray-500 bg-opacity-70 backdrop-blur-md">
 
    <div class="text-zinc-100 flex justify-between px-3 py-4 bg-gray-500 bg-opacity-70 backdrop-blur-md">                   
        <div class="flex space-x-2 px-2 py-1">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm bg-blue-500">
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
            </svg>
            <a href="https://www.msn.com/en-us/video" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm hover:bg-slate-500">
            <path stroke-linecap="round" stroke-linejoin="round" d="M5.25 5.653c0-.856.917-1.398 1.667-.986l11.54 6.348a1.125 1.125 0 010 1.971l-11.54 6.347a1.125 1.125 0 01-1.667-.985V5.653z" />
            </svg>
        </a>
        </div>
        <div class="flex space-x-4">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm hover:bg-slate-500">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
            </svg>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm hover:bg-slate-500">
            <path stroke-linecap="round" stroke-linejoin="round" d="M16.023 9.348h4.992v-.001M2.985 19.644v-4.992m0 0h4.992m-4.993 0l3.181 3.183a8.25 8.25 0 0013.803-3.7M4.031 9.865a8.25 8.25 0 0113.803-3.7l3.181 3.182m0-4.991v4.99" />
            </svg>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm hover:bg-slate-500">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>


        </div>
    </div>
    

    <div class="h-[89%] overflow-scroll pr-16 pl-10 grid grid-cols-2 gap-6 pt-10 pb-6">
            <div v-for="item in articles" :key="item.age" class="select-none flex w-72 h-[300px] overflow-hidden rounded-md bg-zinc-700 hover:bg-slate-800 shadow-md hover:shadow-2xl">
                
               <div class="flex flex-col justify-center place-items-center" >
                <img :src="item.urlToImage" alt="" class="relative top-0 w-full h-[200px] rounded-t-md  ">
                <p class="text-xs mt-2 ml-2 text-green-500">{{ item.author }} · {{item.source.name  }} </p>
                <a :href="item.url" target="_blank" class="font-light text-lg text-zinc-100 mt-2 ml-2 mb-8 hover:underline outline-none">{{ item.title }}</a>
               </div>
            </div>

    </div>

</div>
 
</template>

<style scoped>

</style>
