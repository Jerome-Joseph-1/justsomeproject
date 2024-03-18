<template>
  <div id="app">
    <naviListener/>
  </div>
</template>

<script>
import naviListener from './components/naviListener.vue';


export default {
  name: 'App',
  components: {
    naviListener
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
