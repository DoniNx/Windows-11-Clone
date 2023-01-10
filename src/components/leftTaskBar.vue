<script setup>
import {
    ref
} from "vue"


let descriptionData = {thunderstorm:[
    "Thunderstorm with light rain",
    "Thunderstorm with rain", 
    "Thunderstorm with heavy rain", 	
    "Thunderstorm with light drizzle", 
	"Thunderstorm with drizzle",
	"Thunderstorm with heavy",
	"Thunderstorm with Hail"
] ,

	rain:[
    "Light Drizzle",
	"Drizzle", 
	"Heavy Drizzle", 
	"Light Rain", 
	"Moderate Rain", 	
	"Heavy Rain",
	"Freezing rain", 	
	"Light shower rain",
	"Shower rain", 	
	"Heavy shower rain",
	"Unknown Precipitation"
] ,

	snow:[
    "Light snow",
    "Heavy snow",
    "Snow",
	"Mix snow/rain", 
    "Sleet",	 	
	"Heavy sleet", 
	"Snow shower", 	
	"Heavy snow shower", 	
	"Flurries"
    ],

	mist:[
    "Mist", 	
	"Smoke", 
	"Haze",	
	"Sand/dust", 
	"Fog", 	
    "Freezing Fog" 
    ]	,

    sunny:[
	"Clear sky"	
    ],
    
	fewClouds:[
    "Few clouds",
    "Scattered clouds", 	
	"Broken clouds", 
    ],

    cloudy:[	
	"Overcast clouds", 
    ]
}

var allProps = defineProps({
    description: String,
    tempInC: Number,
})

var desc = "Sunny", weatherIcon = "../src/assets/icons/weather/003-cloudy.png";



console.log("message", allProps.tempInC);



</script>

<template>
<div title="Weather and News" class="w-36  mx-3 px-2 py-1 flex flex-row space-x-2 justify-start place-items-center rounded-[4px] hover:bg-slate-700">
    <img :src="weatherIcon" alt="wIcon" class="h-7">
    <div class="text-xs text-zinc-100 font-semibold font-mono">
        <p >{{ allProps.tempInC || '0'   }}<sup>o</sup>C</p>
        <p >{{ allProps.description || "Undetermined" }} </p>
    </div>
</div>
</template>

<style scoped>
</style>
