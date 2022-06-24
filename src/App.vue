<template>
  <div id="app">
    <CostCalculator/>
  </div>
</template>

<script>
import CostCalculator from './components/CostCalculator.vue'

export default {
  name: 'App',
  components: {
    CostCalculator
  }
}
</script>

<style>
html {
  background-color: #f9faf9;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-left: 32px;
  margin-top: 32px;
  margin-right: 32px;
  color: #000;
}
</style>
