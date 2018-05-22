<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <VisNetwork />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VisNetwork from './components/VisNetwork.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    VisNetwork
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
}
</style>
