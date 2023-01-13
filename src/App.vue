<template>
  <div id="app">
    <Navbar />
<router-view />
    
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/NavBar.vue'
import Footer from '@/components/Footer.vue'
export default{
  components : {Navbar, Footer}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background-color: transparent;
  position: fixed;
}

nav a {
  font-weight: bold;
  font-size: 1.4rem;
  padding-right: 2rem;
  color: #111;
  text-decoration: none;
}

nav a:hover {
  color: crimson;
}

nav a.router-link-exact-active {
  color: crimson;
}
</style>
