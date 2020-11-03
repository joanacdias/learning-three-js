<template>
  <div id="app">
    <Playground msg="Learning Three.js"/>
  </div>
</template>

<script>
import Playground from './views/components/Playground.vue'

export default {
  name: 'App',
  components: {
    Playground
  }
}
</script>

<style lang="scss">
@import './styles/variables';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body {
  margin: 0;
  background-color: $c-background;
}
</style>
