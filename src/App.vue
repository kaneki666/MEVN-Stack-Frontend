<template>
  <div id="app">
    <Navbar />
      <router-view />
  </div>
</template>

<script>
import Products from './components/Products.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'app',
  components: {
    Products,
    Navbar,
    bgc: {
			backgroundColor: ''
		}
  }
  
}
</script>

<style>
body{
  background-color:#20242A;
}

</style>
