<script setup>
import { ref } from 'vue'


</script>

<template>


<div class="rounded-lg mt-10 mx-auto w-[47%] h-[87vh] overflow-hidden flex flex-col justify-between shadow-2xl shadow-gray-900">

<div class=" text-zinc-100 flex justify-center px-7 py-6 bg-zinc-900 bg-opacity-80 backdrop-blur-lg ">                   
        <input class="w-full place-items-center border-b-4 px-2 py-1 border-indigo-500 rounded-sm bg-zinc-800 focus:outline-none" type="text" name="" id="" placeholder=" 🔍 Type here to search">
</div>

<div class="cardsContainer grid grid-cols-2 gap-4 px-16 bg-zinc-900 bg-opacity-80 backdrop-blur-lg h-full overflow-scroll">
    <div v-for="item in arr" :key="item.age" class=" col-span-1 rounded-[5px] text-zinc-50 py-1 px-2 bg-gray-800 hover:bg-sky-700 hover:shadow-2xl">
        <h1 class="text-lg font-bold">{{ item.title }}</h1>
        <p class="text-red-300">age: {{ item.age }}</p>
        <p>{{ item.age }}</p>
        <h5>{{ item.content }}</h5>    
    </div>
</div>


<div class="text-zinc-100 flex justify-between px-14 py-4 bg-zinc-900 zinc-900 bg-opacity-80 backdrop-blur-lg shadow-2xl">                   
    <div class="flex flex-row place-items-center space-x-2 pr-4 font-mono rounded-sm hover:bg-zinc-800 ">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
        </svg>
        DoniVerse
    </div>
    <div class="flex space-x-4">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10 p-2 rounded-sm hover:bg-zinc-800">
  <path stroke-linecap="round" stroke-linejoin="round" d="M5.636 5.636a9 9 0 1012.728 0M12 3v9" />
</svg>

    </div>
</div>


</div>

</template>
<style scoped>

</style>
