<script setup>
import { ref } from 'vue'



let smallIcons = [
    {
        appName: "Telegram",
        iconImg: '../src/assets/icons/smallIcons/telegram.png'
    },
    {
        appName: 'Microsoft',
        iconImg: '../src/assets/icons//smallIcons/microsoft.png'
    },
    {
        appName: 'Avast',
        iconImg: '../src/assets/icons/smallIcons/avast.png'
    },
        {
        appName: 'Bluetooth',
        iconImg: '../src/assets/icons/smallIcons/bluetooth.png'},
        {
        appName: 'Skype',
        iconImg: '../src/assets/icons/smallIcons/skype.png'},
        {
        appName: 'Proton mail',
        iconImg: '../src/assets/icons/smallIcons/proton.png'},

];



function handleClick(theAppName){
    if(theAppName == 'Telegram')
        window.open('https://t.me/doniverse', '_blank')
    else if(theAppName == 'Proton mail')
        window.open('https:/mail.google.com/', '_blank')
}




</script>

<template>



<div class="absolute right-48 bottom-14 rounded-lg  w-28 h-20 overflow-hidden transition-opacity duration-700 bg-zinc-900 bg-opacity-70 backdrop-blur-sm grid grid-cols-3">



<button v-for="icon in smallIcons" :key="icon.appName" :title="icon.appName" @click="handleClick(icon.appName)" class=" flex place-content-center place-items-center align-middle hover:bg-gray-800/60 outline-none">
    <a href="mailto:donifekadu@gmail.com" class="outline-none" v-if="icon.appName=='Proton mail'">
        <img  :src="icon.iconImg" class="w-4 outline-none"  :alt="icon.appName" >
    </a>
    
    <img v-else :src="icon.iconImg" class="w-4 outline-none"  :alt="icon.appName" >

    
</button>





</div>
 
</template>

<style scoped>

</style>
