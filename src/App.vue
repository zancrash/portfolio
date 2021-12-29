<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Home msg="Farzan Ali" tagline="Full Stack Developer"/>
  <!-- <Projects/> -->
</template>

<script>
import Home from './components/Home.vue'
// import Projects from './components/Home.vue'


export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2c3e50; */
  /* margin-top: 60px; */
}
body{
  background: #211d2d;
  margin: 0;
}

body::-webkit-scrollbar {
  width: 7px;               /* width of the entire scrollbar */
}

body::-webkit-scrollbar-track {
  background: #211d2d;        /* color of the tracking area */
}

body::-webkit-scrollbar-thumb {
  background-color: #5dedcd;    /* color of the scroll thumb */
  border-radius: 15px;       /* roundness of the scroll thumb */
}

</style>
