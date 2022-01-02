<template>

  <Menu/>

  <div class="hero">
    <div class="name">
      <!-- <p>Hi, my name is</p> -->
      <h1>{{ msg }}</h1>
    </div>
    <div class="tagline">
      <!-- <p>I'm a ...</p> -->
      <h3>{{ tagline }}</h3>
    </div>
    <div class="external">
      <!-- <fa icon="coffee"/> -->
      <a href="https://github.com/zancrash" target="blank">
        <fa :icon="['fab', 'github']" />
      </a>
      <a href="https://www.linkedin.com/in/farzan-ali-b16b82a4/" target="blank">
        <fa :icon="['fab', 'linkedin']" />
      </a>
    </div>
  </div>
  <Projects/>

  <div id="cta">
    <h2>Check out more of my work on my <a href="https://github.com/zancrash" target="_blank">Github!</a></h2>
    <h2>Or</h2>
    <a href="mailto:farzanali1296@gmail.com">
      <Button><fa :icon="['fas', 'envelope']" />  Get in Touch</Button>
    </a>
  </div>


  <Footer/>


</template>

<script>
import Projects from './Projects.vue';
import Menu from './Menu.vue'
import Footer from './Footer.vue'
export default {
  name: 'Home',
  props: {
    msg: String,
    tagline: String
  },
  components: {
    Menu,
    Projects,
    Footer
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

  .name p{
    color: #5dedcd;
    font-family: 'Roboto Mono', monospace;
  }
  .name h1{
    /* color: #8bc2ad; */
    color: #fff;
    font-size: 10em;
    margin: 0;
  }
  .tagline h3{
    margin: 0;
    font-family: 'Roboto Mono', monospace;
    font-size: 2.7em;
    font-weight: lighter;
    color: #5dedcd;
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
    color: #c278ff;
    font-size: 1.4em;
    transition: all 0.1s linear;

  }

  .external a:hover{
    color: #5dedcd;
  }

  #cta{
    margin: 0 0 100px 0;
  }

  #cta h2{
    color: #fff;
    margin: 20px 0 20px 0;
  }
  #cta h2 a{
    color: #5dedcd;
    text-decoration: none;
    background-color: #003328;
    transition: transform 0.25s ease-out;
  }

  /* #cta h2 a:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #5dedcd;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  } */

  #cta h2 a:hover {
    /* text-decoration: underline; */
    border-bottom: 1px #5dedcd ;
  }


  #cta button{
    width: 250px;
    height: 86px;
    font-size: 22px;
    font-family: 'Roboto Mono', monospace;
    /* background: linear-gradient(45deg, transparent 5%, #826ec0 5%); */
    background-color: #211d2d;
    border: 3px solid #5dedcd;
    color: #fff;
    /* letter-spacing: 3px; */
    /* line-height: 88px; */
    /* box-shadow: 6px 0px 0px #5dedcd; */
    outline: transparent;
    position: relative;
    transition: all 0.1s linear;
  }

  #cta button:hover{
    cursor: pointer;
    color: #fff;
    background-color: #5dedcd;
  }

  /* 1024px wide or less */
  @media screen and (max-width: 1024px) {
    .name h1 {
      font-size: 7em;
    }
    .tagline h3{
      font-size: 2.5em;
    }

    .external a{
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

    .name h1 {
      font-size: 6em;
    }
    .tagline h3{
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
    .name h1{
      font-size: 5em;
    }
    .tagline h3{
      font-size: 1.8em;
    }
  }

  /* 450px wide or less */
  @media screen and (max-width: 450px) {
    .name h1 {
      font-size: 4.5em;
    }
    .tagline h3{
      font-size: 1.5em;
    }

  }

  /* 400px wide or less */
  @media screen and (max-width: 400px) {
    .name h1 {
      font-size: 4em;
    }
    .tagline h3{
      font-size: 1.4em;
    }

  }

</style>
