<script setup>

import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import leftTaskBar from './components/leftTaskBar.vue'
import rightTaskBar from './components/rightTaskBar.vue'
import middleTaskBar from './components/middleTaskBar.vue'
import widgets from './components/widgets.vue'
import Start from './components/start.vue'
import {TransitionRoot, TransitionChild} from '@headlessui/vue'

let toogleWidgets = ref(false)
let toogleStart = ref(false)

</script>

<template>
   <div class="container min-w-full min-h-screen">  
    <TransitionRoot :show="toogleWidgets" 
                    enter="transition transform duration-300 ease-out" 
                    enter-from="-translate-x-8 opacity-0" 
                    enter-to="-translate-x-0 opacity-100" 
                    leave="transition transform duration-300 ease-in" 
                    leave-from="opacity-100" 
                    leave-to="-translate-x-4 opacity-0">
      <widgets />
    </TransitionRoot> 

    <TransitionRoot :show="toogleStart" 
                    enter="transition transform duration-200 ease-out" 
                    enter-from="translate-y-12" 
                    enter-to="translate-y-0 " 
                    leave="transition transform duration-200 ease-in" 
                    leave-from="translate-y-0 opacity-100" 
                    leave-to="translate-y-48 opacity-70">
      <Start />
    </TransitionRoot> 
    
    <div class="taskBar absolute bottom-0 w-full min-w-[854px] py-0  bg-slate-900 flex-row inline-flex justify-between place-items-center">

      <leftTaskBar @click="toogleWidgets = !toogleWidgets" />
        <middleTaskBar @toogle-start-event="toogleStart = !toogleStart"/>
        <rightTaskBar />
        
      </div>

  </div>
</template>

<style scoped>

</style>
