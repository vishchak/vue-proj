<template>
  <div id="app">
    <MySkills/>
  </div>
</template>

<script>
import MySkills from './components/skills.vue'

export default {
  name: 'App',
  components: {
    MySkills
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
