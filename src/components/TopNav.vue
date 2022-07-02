<template lang="html">
  <div class="px-3 py-4 flex items-center justify-between">
     <div class="flex items-center">
         <button class="rounded-full hover:bg-light p-3 flex items-center justify-center" type="button" name="button">
             <img src="logo.png" alt="logo" class="h-6 w-6">
         </button>
         <button  v-for="(item, i) in tabItems" :key ="i" @click="selectedTab = item.key" class= "  rounded-full py-3 px-4 font-semibold" type="button" name="button">
             {{ item.name }}

         </button>
     </div>
     <div class="flex-grow relative">
         <span class="material-icons absolute mt-3 ml-3 text-gray-600">search</span>
         <input class="w-full hover:bg-gray-300 rounded-full bg-gray-200 py-3 pr-3 pl-10" placeholder="Search" name="" value="">

     </div>
     <div class="flex items-center">
         <button type="button" name="button" class="relative rounded-full hover:bg-gray-200 flex items-center justify-center py-2 px-3">
             <span class="material-icons text-2xl text-gray-500">notifications</span>
             <div class="primary rounded-full h-4 w-4 text-white flex items-center justify-center absolute mb-5 ml-5">4</div>
         </button>
          <button type="button" name="button" class="relative rounded-full hover:bg-gray-200 flex items-center justify-center py-2 px-3">
             <span class="material-icons text-2xl text-gray-500">textsms</span>
             <div class="primary rounded-full h-4 w-4 text-white flex items-center justify-center absolute mb-5 ml-5">1</div>
         </button>
         <button class="rounded-full hover:bg-gray-200 p-3 flex items-center justify-center" type="button" name="button">
            <div class="w-6 h-6 bg-cover bg-center rounded-full" style="background-image: url(profile.jpg)"></div>
         </button>
         <button class="w-6 h-6 hover:bg-gray-200 rounded-full flex items-center justify-center" type="button" name="button">
           <span class="material-icons  text-gray-500">expand_more</span>
         </button>
     </div>
  </div>
</template>

<script>

export default {
    data() {
    return {
    tabItems:[
        {name: 'Home', key:'home'},
        {name: 'Today', key:'today'}

    ],
    selectedTab: 'home'
    
    
  }
 }
}
</script>

<style>
.primary {background:#E60023;}
</style>