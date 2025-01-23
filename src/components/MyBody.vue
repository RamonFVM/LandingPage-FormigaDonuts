<template>
  <div class="relative h-screen">
  
    <div class="absolute inset-0 bg-cover bg-center filter blur-md" :style="{ backgroundImage: 'url(' + require('@/assets/background.jpeg') + ')' }"></div>

    <div class="flex justify-center items-center m-10 z-10">
      <div class="bg-[#ffffd0] p-8 rounded-lg shadow-lg max-w-2xl w-3/4">
        <p class="font-semibold text-2xl text-center space-y-4">
          <span class="hover:text-fuchsia-300 text-3xl font-bold">Olá, nós somos a <span class="text-fuchsia-500">Formiga Donuts</span> </span>
          <span class="hover:text-fuchsia-300">, Uma micro empresa dedicada à confecção e venda de mini cakes e donuts deliciosos.</span>
          <br />
          <span class="hover:text-fuchsia-300">Nossos produtos são feitos com ingredientes de <span class="font-semibold text-fuchsia-500">excelente qualidade</span>, para garantir a melhor experiência a cada mordida.</span>
          <br />
          <span class="hover:text-fuchsia-300">De acordo com a sua preferência, realizamos orçamentos personalizados, incluindo todas as taxas de serviço.</span>
          <br />
          <span class="hover:text-fuchsia-300">Conheça nossas delícias e descubra o sabor que vai conquistar seu paladar!</span>
          <br>
        </p>
      </div>
    </div>

    
    <div class="inset-0 flex justify-center items-center m-19 z-20 ">
      <div class="w-full max-w-4xl px-4 rounded-lg overflow-hidden shadow-lg p-6 ">
        <div class="bg-white rounded-2xl shadow-lg overflow-hidden p-4">
          <DonutCard />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DonutCard from './DonutCard.vue';  

export default {
  name: 'MyBody',
  components: {
    DonutCard, 
  },
};
</script>

<style scoped>

.absolute {
  background-size: cover;
  background-position: center;
  filter: blur(8px); 
  z-index: -1; 
}


.w-full {
  max-width: 100%; 
}

.max-w-4xl {
  max-width: 600px; 
}


.rounded-lg {
  border-radius: 15px; 
}

.overflow-hidden {
  overflow: hidden;
}

.shadow-lg {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
}


.donut-card-wrapper img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 10px; 

}

@media (max-width: 768px) {
  .max-w-4xl {
    max-width: 100%;
  }
}
</style>