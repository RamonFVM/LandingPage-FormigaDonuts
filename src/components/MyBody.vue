<template>
  <div class="flex flex-col items-center m-2 z-10 space-y-8">
   
    <div class="bg-[#ffffd0] p-6 sm:p-8 rounded-lg shadow-lg max-w-2xl w-3/4 sm:w-2/3 md:w-1/2">
      <p class="font-semibold text-xl sm:text-2xl text-center space-y-4">
        <span class="hover:text-fuchsia-300 text-3xl font-bold">Olá, nós somos a <span class="text-fuchsia-500">Formiga Donuts</span> </span>
        <span class="hover:text-fuchsia-300">, uma microempresa dedicada à confecção e venda de mini cakes e donuts deliciosos.</span>
        <br />
        <span class="hover:text-fuchsia-300">Nossos produtos são feitos com ingredientes de <span class="font-semibold text-fuchsia-500">excelente qualidade</span>, para garantir a melhor experiência a cada mordida.</span>
        <br />
        <span class="hover:text-fuchsia-300">De acordo com a sua preferência, realizamos orçamentos personalizados, incluindo todas as taxas de serviço.</span>
        <br />
        <span class="hover:text-fuchsia-300">Conheça nossas delícias e descubra o sabor que vai conquistar seu paladar!</span>
      </p>
    </div>
    <div class="bg-[#ffffd0] p-6 sm:p-8 rounded-lg shadow-lg max-w-xl sm:w-3/4 md:w-2/3 text-center">
      <p class="font-bold text-xl sm:text-2xl">
        O preparo é feito com todo o cuidado possível, para que você possa ter a melhor experiência. Esperamos que goste dos nossos produtos! <br />
        Confira um pouco do que temos e esperamos que você tenha uma experiência sensacional.
      </p>
    </div>
  </div>
</template>

<style scoped>

@media (max-width: 768px) {
  .max-w-2xl {
    max-width: 100%;
  }

  .max-w-xl {
    max-width: 100%;
  }

  .text-xl {
    font-size: 1rem;
  }

  .sm\:text-2xl {
    font-size: 1.25rem;
  }

  .p-6 {
    padding: 1.5rem;
  }

  .p-8 {
    padding: 2rem;
  }
}
</style>