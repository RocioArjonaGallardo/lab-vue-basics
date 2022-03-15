<template>
  <div id="app">
    <NavBar />
    <router-view/> 
    <BooleanData />
    <Footer />
  </div>
</template>
<script>
import Footer from '@/components/Footer.vue'
import NavBar from '@/components/NavBar.vue'
import HelloWorld from '@/components/HelloWorld.vue'
import BooleanData from '@/components/BooleanData.vue'


export default {
  name: 'HomeView',
  components: {
    Footer,
    NavBar,
    HelloWorld,
    BooleanData,
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 3.75rem;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 1rem;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
