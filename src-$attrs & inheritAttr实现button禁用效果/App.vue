<template>
  <div id="app">
    <Parent></Parent>
    <Button disabled></Button>
  </div>
</template>

<script>
import Parent from './components/Parent'
import Button from './components/Button';

export default {
  name: 'App',
  components: {
    Parent,
    Button
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
