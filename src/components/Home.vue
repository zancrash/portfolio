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

      <!-- <a href="https://www.linkedin.com/in/farzan-ali-b16b82a4/" target="blank">
        <fa :icon="['fab', 'google-play']" />
      </a> -->

      
      <!-- <a href="https://www.linkedin.com/in/farzan-ali-b16b82a4/" target="blank">
        <fa :icon="['fas', 'external-link-alt']" />
      </a> -->

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
  .name{
    width: 80%;
    max-width: 1344px;
  }
  h1{
    /* color: #8bc2ad; */
    color: #fff;
    font-size: 10em;
    margin: 0;
  }
  h3{
    margin: 0;
    font-size: 2.7em;
    font-weight: lighter;
    color: #fff;
  }
  .external{
    /* min-width: 150px;
    max-width: 6vw; */
    width: 200px;
    display: flex;
    justify-content: space-around;
    font-size: 3em;
    color: yellow;
    margin: 120px 0 10px 0;
  }

  .external a{
    color: #5dedcd;
    font-size: 1.4em;
  }

  .external a:hover{
    color: #2eff74;
  }

  /* 1024px wide or less */
  @media screen and (max-width: 1024px) {
    h1 {
      font-size: 7em;
    }
    h3{
      font-size: 2.5em;
    }

    .external a{
      color: #5dedcd;
      font-size: 1.4em;
    }
  }

  /* 800px wide or less */
  @media screen and (max-width: 800px) {

    .external a{
      font-size: 1.4em;
    }

  }

  /* 700px wide or less */
  @media screen and (max-width: 700px) {

    h1 {
      font-size: 6em;
    }
    h3{
      font-size: 2em;
    }

    .external{
      width: 150px;
    }

    .external a{
      font-size: 1.2em;
    }

  }


  /* 600px wide or less */
  @media screen and (max-width: 600px) {
    h1{
      font-size: 5em;
    }
    h3{
      font-size: 1.8em;
    }
  }

  /* 450px wide or less */
  @media screen and (max-width: 450px) {
    h1 {
      font-size: 3.8em;
    }
    h3{
      font-size: 1.5em;
    }

  }

  /* 400px wide or less */
  @media screen and (max-width: 400px) {
    h1 {
      font-size: 3.5em;
    }
    h3{
      font-size: 1.4em;
    }

  }

</style>
