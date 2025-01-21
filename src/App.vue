<template>
  <div id="app">
    <MyHeader />
    <MyBody/>
  </div>
</template>

<script>

import MyHeader from './components/MyHeader.vue'
import MyBody from  './components/MyBody.vue'

export default {
  name: 'App',
  components: {
    MyBody,
    MyHeader
  }
}
</script>

