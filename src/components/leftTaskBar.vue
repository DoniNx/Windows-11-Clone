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
    isWeatherFetched: Boolean
})
var desc = "Sunny", weatherIcon = "../src/assets/icons/weather/003-cloudy.png";


// while(!allProps.isWeatherFetched){
//   if (descriptionData.thunderstorm.includes(allProps.description)) {
//   desc = "Thunderstorm";
//   weatherIcon = "../src/assets/icons/weather/thunderstorm.png";
// } else if(descriptionData.rain.includes(allProps.description)) {
//   desc = "Rain";
//   weatherIcon = "../src/assets/icons/weather/rain.png";
// } else if(descriptionData.cloudy.includes(allProps.description)) {
//   desc = "Cloudy";
//   weatherIcon = "../src/assets/icons/weather/cloud.png";
// }  else if(descriptionData.snow.includes(allProps.description)) {
//   desc = "Snow";
//   weatherIcon = "../src/assets/icons/weather/snow.png";
// }  else if(descriptionData.mist.includes(allProps.description)) {
//   desc = "Fog";
//   weatherIcon = "../src/assets/icons/weather/fog.png";
// }  else if(descriptionData.fewClouds.includes(allProps.description)) {
//   desc = "Light clouds";
//   weatherIcon = "../src/assets/icons/weather/partlyCloud.png";
// }  else if(descriptionData.sunny.includes(allProps.description)) {
//   desc = "Clear sky";
//   weatherIcon = "../src/assets/icons/weather/sun.png";
// }else{
//   desc = "Sunny";
//   weatherIcon = "../src/assets/icons/weather/003-cloudy.png";
// }
// }




</script>

<template>
<div title="Weather and News" class="w-36  mx-3 px-2 py-1 flex flex-row space-x-2 justify-start place-items-center rounded-[4px] hover:bg-slate-700">
    <img :src="weatherIcon" alt="weatherIcon" class="h-7">
    <div class="text-xs text-zinc-100 font-semibold font-mono">
        <p >{{ Math.round(allProps.tempInC) || '0'   }}<sup>o</sup>C</p>
        <p >{{ allProps.description }}</p>
    </div>
</div>
</template>

<style scoped>
</style>
