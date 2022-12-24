<script setup>
import HelloWorld from './components/HelloWorld.vue'
import leftTaskBar from './components/leftTaskBar.vue'
import rightTaskBar from './components/rightTaskBar.vue'
import middleTaskBar from './components/middleTaskBar.vue'
</script>

<template>
   <div class="container min-w-full min-h-screen">
    
    <div class="taskBar absolute bottom-0 w-full min-w-[854px] py-0  bg-slate-900 flex-row inline-flex justify-between place-items-center">
        <leftTaskBar />
        <middleTaskBar />
        <rightTaskBar />
        
      </div>

  </div>
</template>

<style scoped>

</style>
