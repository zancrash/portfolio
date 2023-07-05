<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Home msg="Farzan Ali" tagline="Software Developer"/>
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
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@200;300;400;500;600&family=Roboto+Mono:wght@300;400&display=swap');
#app {
  font-family: 'Kanit', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
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
