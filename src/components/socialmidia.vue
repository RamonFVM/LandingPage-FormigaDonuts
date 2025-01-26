<template>
  <div>
    
    <a href="https://www.instagram.com/formiga_donuts/" target="_blank" class="fixed-icon instagram">
      <span class="material-icons">instagram</span>
    </a>

   
    <a href="https://wa.me/1234567890" target="_blank" class="fixed-icon whatsapp">
      <span class="material-icons">whatsapp</span>
    </a>
  </div>
</template>

<script>
export default {
  name: "FixedIcons",
};
</script>

<style scoped>

.fixed-icon {
  position: fixed;
  bottom: 20px;
  background-color: #ff4081;
  padding: 15px;
  border-radius: 50%;
  color: white;
  font-size: 24px;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s ease, transform 0.3s ease;
  z-index: 1000;
}


.instagram {
  right: 80px; 
}

.whatsapp {
  right: 20px; 
}


.fixed-icon:hover {
  transform: scale(1.1);
}

.instagram:hover {
  background-color: #e1306c; 
}

.whatsapp:hover {
  background-color: #25d366; 
}
</style>