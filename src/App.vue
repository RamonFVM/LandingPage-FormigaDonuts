<template>
  <div class="bg-[#fee9e8]" id="app">
    <MyHeader />
    <MyBody/>
    <DonutCard/>
    <ListProducts/>
    
  </div>
</template>

<script>

import MyHeader from './components/MyHeader.vue'
import MyBody from  './components/MyBody.vue'
import ListProducts from './components/ListProducts.vue';
import DonutCard from './components/DonutCard.vue';

export default {
  name: 'App',
  components: {
    MyBody,
    MyHeader,
    ListProducts,
    DonutCard
  }
}
</script>



