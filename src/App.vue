<template>
  <div id="app">
    <NavBar/>
    <img alt="Vue logo" src="./assets/logo.png">
    <MoviesDb></MoviesDb>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import MoviesDb from './components/MoviesDb'

export default {
  name: 'App',
  components: {
    NavBar,
    MoviesDb
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
 
}
</style>
