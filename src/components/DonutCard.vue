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
        { image: require('@/assets/donut1.jpeg') },
        { image: require('@/assets/donut2.jpeg') },
        { image: require('@/assets/donut3.jpeg') },
        { image: require('@/assets/donut4.jpeg') },
        { image: require('@/assets/donut6.jpeg') },
        { image: require('@/assets/donut7.jpeg') }
      ]
    };
  }
};
</script>

<style scoped>
.card-container {
  position: relative;
  display: grid;  
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));  
  gap: 1rem; 
  width: 100%;
  justify-items: center;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.5); 
  border-radius: 20px;  
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);  
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 10px;
  background-color: transparent; 
  border-radius: 15px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, border 0.3s ease;
  width: 30%; 
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



@media (min-width: 1200px) {
  .card-container {
    grid-template-columns: repeat(2, 1fr); 
  }
  .card {
    width: 30%; 
  }
}


@media (max-width: 1199px) and (min-width: 1024px) {
  .card-container {
    grid-template-columns: repeat(3, 1fr);  
  }
  .card {
    width: 40%; 
  }
}


@media (max-width: 1024px) {
  .card-container {
    grid-template-columns: repeat(2, 1fr); 
  }
  .card {
    width: 45%; 
  }
}


@media (max-width: 768px) {
  .card-container {
    grid-template-columns: 1fr;  
  }
  .card {
    width: 80%; 
  }

}
</style>