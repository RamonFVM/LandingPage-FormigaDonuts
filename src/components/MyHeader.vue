<template>
     
  

    <div class="flex bg-fuchsia-300 justify-center items-center m-0 p-14">
        <img 
        :src="require('@/assets/donuts.png')" 
        alt="Imagem Girando"
        class="w-32 h-32 mt-6 animate-spin-slow"
      />

      <h1 class="font-mono text-purple-700 text-5xl">
        Formiga Donuts
      </h1>
      
      <img 
        :src="require('@/assets/donuts.png')" 
        alt="Imagem Girando"
        class="w-32 h-32 mt-6 animate-spin-slow"
      />
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
  }
  </script>
  
  <style scoped>
  @keyframes spinSlow {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  
  .animate-spin-slow {
    animation: spinSlow 4s linear infinite; 
  }
  </style>