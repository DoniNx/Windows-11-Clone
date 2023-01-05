<script setup>

import { onBeforeMount, ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import leftTaskBar from './components/leftTaskBar.vue'
import rightTaskBar from './components/rightTaskBar.vue'
import middleTaskBar from './components/middleTaskBar.vue'
import widgets from './components/widgets.vue'
import SmallIcons from './components/SmallIcons.vue'
import Start from './components/start.vue'
import ButtonsMenu from './components/buttons.vue'
import CalendarMenu from './components/calendarMenu.vue'
import {TransitionRoot, TransitionChild} from '@headlessui/vue'



let toogleWidgets = ref(false)
let toogleStart = ref(false)
let toogleButtons = ref(false)
let toogleSmallIcons = ref(false)
let toogleCaledar = ref(false)


//News functions
let myArticles =ref([]);
let myWeather =ref({});


let desc ='', tempr=0, isFetched = {weather: false, news: false};
onBeforeMount(async ()=>{
    fetch("https://newsapi.org/v2/top-headlines?sources=techcrunch&apiKey=241f920926d34fbc8debd79c155324d4").then((res)=>res.json()).then((data)=> {
    myArticles = data.articles 
    isFetched.news = true
    })
    

    
   fetch("https://api.openweathermap.org/data/2.5/weather?lat=8.9806&lon=38.7578&appid=de88c8fbc80c77a7fad3b13e1477d052").then((res)=>res.json()).then((data)=> {
    myWeather = data
    desc=myWeather.weather[0].description;
    tempr= Math.round(myWeather.main.temp - 273);
    isFetched.weather = true;

 })


})

</script>

<template>
   <div class="container min-w-full min-h-screen">  
    <TransitionRoot :show="toogleWidgets" 
                    enter="transition transform duration-200 ease-out" 
                    enter-from="-translate-x-8 opacity-0" 
                    enter-to="-translate-x-0 opacity-100" 
                    leave="transition transform duration-300 ease-in" 
                    leave-from="opacity-100" 
                    leave-to="-translate-x-72 opacity-80">
      <widgets :articles="myArticles" :weatherWidget="myWeather"/>
    </TransitionRoot> 

    <TransitionRoot :show="toogleStart" 
                    enter="transition transform duration-200 ease-out" 
                    enter-from="translate-y-12" 
                    enter-to="translate-y-0 " 
                    leave="transition transform duration-200 ease-in" 
                    leave-from="translate-y-0 opacity-100" 
                    leave-to="translate-y-56 opacity-70">
      <Start />
    </TransitionRoot> 

      <SmallIcons v-show="toogleSmallIcons" />

    <TransitionRoot :show="toogleCaledar" 
    enter="transition transform duration-200 ease-out" 
                    enter-from="-translate-x-8 opacity-0" 
                    enter-to="translate-x-0 opacity-100" 
                    leave="transition transform duration-300 ease-in" 
                    leave-from="opacity-100" 
                    leave-to="translate-x-72 opacity-80">
      <CalendarMenu  />
    </TransitionRoot>
    
    <TransitionRoot :show="toogleButtons" 
    enter="transition transform duration-100 ease-out" 
                    enter-from="translate-y-14 opacity-20" 
                    enter-to="translate-y-0 opacity-100 " 
                    leave="transition transform duration-100 ease-in" 
                    leave-from="opacity-100 translate-y-0" 
                    leave-to="opacity-90 translate-y-56">
      <ButtonsMenu  />
    </TransitionRoot> 

    <div class="taskBar absolute bottom-0 w-full min-w-[854px] py-0  bg-slate-900 flex-row inline-flex justify-between place-items-center">
      <leftTaskBar :description="desc" :tempInC="tempr" :isWeatherFetched="isFetched.weather" @click="toogleWidgets = !toogleWidgets" />
        <middleTaskBar @toogle-start-event="toogleStart = !toogleStart"/>
        <rightTaskBar 
          @toogle-buttons-event="toogleButtons = !toogleButtons"  
          @toogle-small-icons-event="toogleSmallIcons = !toogleSmallIcons"
          @toogle-calendar-event="toogleCaledar = !toogleCaledar"/>
      </div>
  </div>
</template>

<style scoped>

</style>
