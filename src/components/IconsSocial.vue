<template>
    <div>
      <button @click="toggleSocial" class="fixed-button">
        Clique aqui para visitar
      </button>
  
      <div v-if="Social" class="overlay">
        <div class="card">
          <a href="https://www.instagram.com/formiga_donuts/" target="_blank" class="fixed-icon instagram">
            <span class="material-icons">instagram</span>
          </a>
  
          <a href="https://wa.me/558399853196" target="_blank" class="fixed-icon whatsapp">
            <span class="material-icons">whatsapp</span>
          </a>
  
          <button @click="toggleSocial" class="close-btn">X</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        Social: false, 
      };
    },
    methods: {
      toggleSocial() {
        this.Social = !this.Social;
      }
    }
  };
  </script>
  
  <style scoped>
  .fixed-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #ff4081;
    padding: 20px 40px;
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
  
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6);
    backdrop-filter: blur(8px);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 999;
  }
  
  .card {
    background-color: white;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
    width: 60%; 
    max-width: 500px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  
  .fixed-icon {
    position: relative;
    bottom: 20px;
    background-color: #ff4081;
    padding: 20px;
    border-radius: 16px;
    color: white;
    font-size: 24px;
    text-decoration: none;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    margin: 15px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    transition: background-color 0.3s ease, transform 0.3s ease;
    z-index: 1000;
  }
  
  .instagram:hover {
    background-color: #e1306c;
  }
  
  .whatsapp:hover {
    background-color: #25d366;
  }
  
  .fixed-icon:hover {
    transform: scale(1.1);
  }
  
  .close-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    background-color: #ff4081;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 50%;
    cursor: pointer;
    margin-top: 30px;
  }
  
  .close-btn:hover {
    background-color: #f50057;
  }
  
  @media (max-width: 768px) {
    .fixed-button {
      width: 60%;
      right: 20px;
      bottom: 15px;
      font-size: 14px;
      padding: 16px 32px;
    }
  
    .card {
      width: 75%;  
      padding: 30px; 
    }
  
    .fixed-icon {
      padding: 25px;
      font-size: 28px;
      margin: 25px;
    }
  
    .close-btn {
      padding: 12px 24px;
      margin-top: 40px;
    }
  }
  
  @media (max-width: 480px) {
    .fixed-button {
      width: 70%;
      right: 10px;
      bottom: 10px;
      font-size: 14px;
      padding: 12px 24px;
    }
  
    .card {
      width: 85%; 
      padding: 35px;
    }
  
    .fixed-icon {
      padding: 18px;
      font-size: 26px;
      margin: 30px;
    }
  
    .close-btn {
      padding: 8px 16px;
      margin-top: 50px;
    }
  }
  </style>