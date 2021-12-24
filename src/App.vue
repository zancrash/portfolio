<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Home msg="Farzan Ali" tagline="Full Stack Developer"/>
</template>

<script>
import Home from './components/Home.vue'

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

</style>
