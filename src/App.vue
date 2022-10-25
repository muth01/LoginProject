<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <Home data="Muthu here!!" msg="I am good"/> -->
    <!-- <New/> -->
    <!-- <Calculator/> -->
    <Demo/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Home from './components/Home.vue'
// import New from './components/New.vue'
// import Calculator from './components/Calculator.vue'
import Demo from './components/Demo.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    // Home,
    // New,
    // Calculator,
    Demo
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
