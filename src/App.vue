<template>
  <div id="app">
    <Nav :style="scrolled"/>
    <!-- <Jumbotron/> -->
  </div>
</template>

<script>
import Nav from './components/Nav'
import Jumbotron from './components/jumbotron/Jumbotron'
export default {
  name: 'App',
  components: {
    Nav,
    Jumbotron
  },
  data () {
    return {
      scrolled: {
        transition: 'min-height 0.5s',
        minHeight: '50vh'
        // max-height: 50vh
      }
    }
},
  methods: {
    onResize (event) {
      if(window.scrollY == 0){
        this.scrolled.minHeight = '50vh';
      } else {
        this.scrolled.minHeight = '10px';
      }
    }
  },

  mounted () {
    // Register an event listener when the Vue component is ready
    window.addEventListener('scroll', this.onResize)
  },

  beforeDestroy () {
    // Unregister the event listener before destroying this Vue instance
    // window.removeEventListener('scroll', this.onResize)
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  min-height: 2000px;
}

  .navbar{
    min-height:50vh;
    max-height: 50vh;
    transition: min-height 0.5s;
  }


h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
