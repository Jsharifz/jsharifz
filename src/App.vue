<template>
  <div id="app">
    <a href="#"
      ><div id="to-top" :style="displayToTop">
        Top
      </div></a
    >
    <Hero />
    <h1 class="title">Skills</h1>
    <Stacks />
    <h1 class="title">Projects</h1>
    <Projects />
    <h1 class="title">Contact</h1>
    <Contact />
    <Footer />
  </div>
</template>

<script>
  import Hero from './components/Hero.vue';
  import Stacks from './components/Stacks';
  import Projects from './components/Projects';
  import Contact from './components/Contact';
  import Footer from './components/Footer';

  export default {
    name: 'App',
    components: {
      Hero,
      Stacks,
      Projects,
      Contact,
      Footer,
    },
    data() {
      return {
        scrollValue: 0,
        displayToTop: '',
      };
    },
    created() {
      document.onscroll = this.updateScrollValue;
      this.displayToTop = {
        opacity: `0%`,
        'margin-bottom': `400px`,
        'pointer-events': 'none',
      };
    },
    methods: {
      updateScrollValue: function() {
        if (this.scrollValue >= 250) {
          this.displayToTop = {
            opacity: `100%`,
            'margin-bottom': `2rem`,
            'pointer-events': 'auto',
          };
        } else {
          this.displayToTop = {
            opacity: `0%`,
            'margin-bottom': `400px`,
            'pointer-events': 'none',
          };
        }
        this.scrollValue = window.scrollY;
      },
    },
  };
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: black;
    margin: 0;
  }

  a {
    color: inherit;
    text-decoration: inherit;
  }

  .title {
    margin-top: 10rem;
  }

  p,
  a,
  form {
    margin: 0;

    font-size: 1.25rem;
    line-height: 1.75rem;
  }

  #to-top {
    display: flex;

    justify-content: center;
    align-items: center;

    font-size: 1rem;

    position: fixed;
    right: 0px;
    bottom: 0px;

    width: 50px;
    height: 50px;
    margin: 2rem;

    border-bottom: solid 0px rgba(255, 255, 255, 0);
    border-radius: 50%;

    background-color: rgb(206, 241, 255);

    z-index: 2;

    transition: 0.25s;
  }

  #to-top:hover {
    transform: rotateX(30deg);

    border-bottom: solid 7px skyblue;
    background-color: rgb(232, 248, 255);
  }

  .displayToTop {
    display: flex !important;
  }
</style>
