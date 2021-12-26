<template>
  <div class="hero">
    <div class="name">
      <h1>{{ msg }}</h1>
    </div>
    <div class="tagline"><h3>{{ tagline }}</h3></div>
    <div class="external">
      <!-- <fa icon="coffee"/> -->
      <a href="https://github.com/zancrash" target="blank">
        <fa :icon="['fab', 'github']" />
      </a>
      <a href="https://www.linkedin.com/in/farzan-ali-b16b82a4/" target="blank">
        <fa :icon="['fab', 'linkedin']" />
      </a>
      <!-- <i class="fab fa-github"></i> -->
    </div>
  </div>
  <Projects/>

</template>

<script>
import Projects from './Projects.vue';
export default {
  name: 'Home',
  props: {
    msg: String,
    tagline: String
  },
    components: {
    Projects
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero{
  width: 100%;
  height: 100vh;
  /* background: #000000; */
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center; /* Vertical justify */
  vertical-align: middle;
}
h1{
  /* color: #8bc2ad; */
  color: #fff;
  font-size: 15vh;
  margin: 0;
}
h3{
  margin: 0;
  font-size: 3vh;
  font-weight: lighter;
  color: #fff;
}
.external{
  min-width: 150px;
  max-width: 6vw;
  display: flex;
  justify-content: space-around;
  font-size: 3em;
  color: yellow;
  margin: 20px 0 10px 0;
}

.external a{
  color: #2eff74;
}

.external a:hover{
  color: yellow;
}
</style>
