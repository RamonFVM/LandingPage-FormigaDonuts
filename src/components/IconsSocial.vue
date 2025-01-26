<template>
    <div>
      <!-- Botão para alternar a visibilidade do socialmidia -->
      <button @click="toggleSocial" class="fixed-button">
        Clique aqui para visitar
      </button>
  
      <!-- Exibe o componente 'socialmidia' com fundo borrado -->
      <div v-if="Social" class="overlay">
        <div class="card">
          <socialmidia />
          <button @click="toggleSocial" class="close-btn">Fechar</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import socialmidia from './socialmidia.vue';
  
  export default {
    components: {
      socialmidia
    },
    data() {
      return {
        Social: false,  // Começa com 'false', o componente não será mostrado
      };
    },
    methods: {
      // Alterna o valor de 'Social' para mostrar ou esconder o componente
      toggleSocial() {
        this.Social = !this.Social;
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos para o botão fixo */
  .fixed-button {
    position: fixed;
    bottom: 20px;
    width: 15%;
    right: 20px;
    background-color: #ff4081;
    padding: 10px 20px;
    border-radius: 5px;
    color: white;
    font-size: 16px;
    border: none;
    cursor: pointer;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    transition: background-color 0.3s ease;
  }
  
  .fixed-button:hover {
    background-color: #f50057;
  }
  
  /* Estilo para o fundo borrado */
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6); /* Fundo escuro */
    backdrop-filter: blur(8px); /* Aplica o desfoque ao fundo */
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 999; /* Garante que a sobreposição fique acima de outros conteúdos */
  }
  
  /* Estilos para o card centralizado */
  .card {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
    width: 80%;
    max-width: 500px;
    text-align: center;
    position: relative;
  }
  
  /* Estilos para o botão de fechar */
  .close-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    background-color: #ff4081;
    color: white;
    border: none;
    padding: 5px 10px;
    border-radius: 50%;
    cursor: pointer;
  }
  
  .close-btn:hover {
    background-color: #f50057;
  }
  </style>