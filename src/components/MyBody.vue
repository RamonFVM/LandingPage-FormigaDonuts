<template>
  <div class="relative h-screen">
    <!-- Imagem de fundo com desfoque -->
    <div class="absolute inset-0 bg-cover bg-center" :style="{ backgroundImage: 'url(' + require('@/assets/background.jpeg') + ')' }"></div>

    <!-- Caixa de conteúdo -->
    <div class="flex justify-center items-center m-10 rounded-2xl">
      <div class="bg-[#ffffd0] p-8 rounded-lg shadow-lg max-w-3xl w-full">
        <p class="font-semibold text-2xl text-center space-y-4">
          <span class="hover:text-fuchsia-300 text-3xl font-bold">Olá, nós somos a <span class="text-fuchsia-500">Formiga Donuts</span> </span>
          <span class="hover:text-fuchsia-300">, Uma microempresa dedicada à confecção e venda de mini cakes e donuts deliciosos.</span>
          <br />
          <span class="hover:text-fuchsia-300">Nossos produtos são feitos com ingredientes de <span class="font-semibold text-fuchsia-500">excelente qualidade</span>, para garantir a melhor experiência a cada mordida.</span>
          <br />
          <span class="hover:text-fuchsia-300">De acordo com a sua preferência, realizamos orçamentos personalizados, incluindo todas as taxas de serviço.</span>
          <br />
          <span class="hover:text-fuchsia-300">Conheça nossas delícias e descubra o sabor que vai conquistar seu paladar!</span>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SobreNos',
};
</script>

<style scoped>
/* Estilo da imagem de fundo com desfoque */
.absolute {
  background-size: cover;
  background-position: center;
  filter: blur(8px);
  z-index: -1;
}
</style>