<template>
  <div class="card-container">
    <div v-for="(item, index) in cards" :key="index" class="card">
      <img :src="item.image" alt="Imagem de Donut" class="card-image" />
      <div class="card-content">
      
       
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DonutCard",
  data() {
    return {
      cards: [
        {
          image: require('@/assets/donut1.jpeg'),
          
        },
        {
          image: require('@/assets/donut2.jpeg'),
          
        },
        {
          image: require('@/assets/donut3.jpeg'),
        
        },
        {
          image: require('@/assets/donut4.jpeg'),
          
        },
       
        {
          image: require('@/assets/donut6.jpeg'),
     
        },
        {
          image: require('@/assets/donut7.jpeg'),
         
        },
        

        
        
      ]
    };
  }
};
</script>

  <style scoped>
  .card-container {
    display: flex;
    justify-content: center; 
    align-items: center;
    gap: 1rem;  
    flex-wrap: wrap; 
  }
  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 10px;
    background-color: #fff;
    border-radius: 15px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: transform 0.3s ease, border 0.3s ease;  
    width: 250px; 
    height: auto;  
  }

  .card:hover {
    transform: scale(1.05);  
    border: 3px solid #ff007f;
  }

  .card-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 10px;
  }

  .card-content {
    margin-top: 10px;
  }

  .card-title {
    font-size: 1.2rem;
    font-weight: bold;
  }

  .card-description {
    font-size: 1rem;
    color: #555;
  }
  </style>