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

@import url('https://fonts.googleleapis.com/css?family=Montserrat:400,700');

body {
  background-color: #eee;
  font-family: 'Montserrat', sans-serif;
  display: grid;
  grid-template-rows: auto;
  justify-items: center;
}

body, html {
  margin: 0;
  height: 100%;
}

#app {
  width: 50%;
}
</style>
