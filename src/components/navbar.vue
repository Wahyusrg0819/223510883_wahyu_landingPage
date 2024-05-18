<template>

  <div class="q-pa-none" id="navbar">
   <q-toolbar class="bg-brown text-white ">
     <q-btn flat round dense icon="menu" class="q-mr-sm" />
     <avatar>
       <img class="gambar" src="../assets/Screenshot_2024-05-18_173246-removebg-preview.png" />
     </avatar>

     

     <q-space />

     <q-btn-toggle
       v-model="model"
       flat stretch
       toggle-color="white"
       :options="options"
     />

     <div class="input-container">
       <input type="text" name="text" class="input" placeholder="search...">
       <span class="icon"> 
         <svg width="19px" height="19px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path opacity="1" d="M14 5H20" stroke="#000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path> <path opacity="1" d="M14 8H17" stroke="#000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path> <path d="M21 11.5C21 16.75 16.75 21 11.5 21C6.25 21 2 16.75 2 11.5C2 6.25 6.25 2 11.5 2" stroke="#000" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"></path> <path opacity="1" d="M22 22L20 20" stroke="#000" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
       </span>
     </div>

     
   </q-toolbar>
 
 </div>
</template>

<script>
import { ref } from 'vue'

export default {
 setup () {
   return {
     model: ref('one'),

     options: [
       { label: 'Login', value: 'one' },
       { label: 'About', value: 'two' },
       { label: 'Contact', value: 'three' }
     ]
   }
 }
}
</script>

<style>

.gambar {
 width: 50%;
 height: auto;
}

.input-container {
 width: 300px;
 position:relative;

}

.icon {
 position: absolute;
 right: 10px;
 top: calc(50% + 5px);
 transform: translateY(calc(-50% - 5px));
}

.input {
 width: 100%;
 height: 40px;
 padding: 10px;
 transition: .2s linear;
 border: 2.5px solid black;
 font-size: 14px;
 text-transform: uppercase;
 letter-spacing: 2px;
}

.input:focus {
 outline: none;
 border: 0.5px solid black;
 box-shadow: -5px -5px 0px black;
}

.input-container:hover > .icon {
 animation: anim 1s linear infinite;
}

@keyframes anim {
 0%,
 100% {
   transform: translateY(calc(-50% - 5px)) scale(1);
 }

 50% {
   transform: translateY(calc(-50% - 5px)) scale(1.1);
 }
}

</style>