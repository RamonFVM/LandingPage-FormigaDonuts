<template>
  <div class="bg-[#fee9e8]" id="app">
    <MyHeader />
    <MyBody/>
    <DonutCard/>
    <ListProducts/>
    <IconsSocial/>

    
  </div>
</template>

<script>

import MyHeader from './components/MyHeader.vue'
import MyBody from  './components/MyBody.vue'
import ListProducts from './components/ListProducts.vue';
import DonutCard from './components/DonutCard.vue';
import IconsSocial from './components/IconsSocial.vue';

export default {
  name: 'App',
  components: {
    MyBody,
    MyHeader,
    ListProducts,
    DonutCard,
    IconsSocial
  }
}
</script>



