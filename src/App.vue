<template>
  <div id="app">
    <Navbar/>
    <Sidebar/>
    <Content/>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import Navbar from './components/Navbar.vue'
import Content from './components/Content.vue'

export default {
  name: 'App',
  components: {
    Sidebar,
    Navbar,
    Content
  }
}
</script>

<style>
#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
