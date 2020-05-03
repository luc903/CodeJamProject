<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/Trump.png" width="500px">

    <intro greeting="Welcome to the trump quote generator"></intro>
    <quote></quote>
  </div>
</template>

<script>

import intro from './components/IntroScreen.vue'
import quote from './components/Quote.vue'

export default {
  name: 'App',
  components: {
    intro,
    quote
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
  margin-top: 60px;
}

button {
  background: transparent;
  border: 1px solid black;
  padding: 10px 25px;
}

</style>
