<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Testing></Testing>
    <Homework></Homework>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Testing from './components/Testing.vue'
import Homework from './components/Homework.vue'

export default {
  name: 'App',
  components: {
    Testing,
    Homework
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
</style>
