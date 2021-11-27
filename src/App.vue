<template>
  <div id="app">
    <Sidebar/>
    <Navbar/>
    <router-view/>
  </div>
</template>
<script>
import Sidebar from '@/components/Sidebar.vue'
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Sidebar,
    Navbar
  }
}
</script>

<style>
#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

ul li a.router-link-exact-active {
  color: #ffc107 !important;
}
</style>
