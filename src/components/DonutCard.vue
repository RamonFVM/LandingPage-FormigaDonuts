<template>
  <div>
    <div ref="splide" class="splide">
      <div class="splide__track">
        <ul class="splide__list">
          <li class="splide__slide" v-for="(item, index) in images" :key="index">
            <img :src="item" alt="Imagem de Donut" class="image-size" />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Splide from '@splidejs/splide';
import '@splidejs/splide/dist/css/themes/splide-sea-green.min.css';

export default {
  name: "DonutCard",
  data() {
    return {
      images: [
        require('@/assets/donut1.jpeg'),
        require('@/assets/donut2.jpeg'),
        require('@/assets/donut3.jpeg'),
        require('@/assets/donut4.jpeg'),
        require('@/assets/donut5.jpeg')
      ]
    };
  },
  mounted() {
    new Splide(this.$refs.splide, {
      type       : 'fade',
      heightRatio: 0.5,
      autoplay  : true,
      arrows    : true,
      prevArrow : '<button class="splide__arrow splide__arrow--prev">←</button>',
      nextArrow : '<button class="splide__arrow splide__arrow--next">→</button>',
      pagination: true,
      speed      : 500
    }).mount();
  }
};
</script>

<style scoped>
.splide__arrow {
  background-color: transparent;
  border: none;
  color: #000; 
  font-size: 2rem; 
  padding: 10px;
  cursor: pointer;
}

.splide__arrow:hover {
  color: #f44336;
}

.splide__pagination button {
  background-color: #000; 
}

.splide__slide img {
  width: 100%;
  height: 200px; 
  object-fit: cover; 
}


.image-size {
  width: 100%;
  height: 200px; 
  object-fit: cover;
}
</style>