<template>
  <div class="skills">
    {{ name }}
    <button v-on:click="changeName" v-bind:disabled="btnState">Change name</button>
  </div>
  <h1 v-once>{{name}}</h1>
{{ btnState ? 'The button is disabled' : 'The button is actives'}}
</template>

<script>
export default {
  name: 'MySkills',
  data() {
    return {
      name: 'Course in Vue',
      btnState: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
