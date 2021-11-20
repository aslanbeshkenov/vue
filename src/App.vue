<template>
  <div id="app">
    <Calc></Calc>
  </div>
</template>

<script>
import Calc from './components/Calc.vue'

export default {
  name: 'App',
  components: {
    Calc,
  },
  data() {
    return {
      counter: 0,
      str: 'hi',
    }
  },
  methods: {
    sum(step, event) {
      console.log(event)
      this.counter += step
    },
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
