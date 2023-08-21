<template>
  <div class="skills">
    <h1 v-once>{{ name }}</h1>
    <button v-on:click="changeName" :disabled="btnState">Change name</button>
    {{ btnState ? 'The button is disabled' : 'The button is active' }}
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key="index">{{ index + 1 }}. {{ data.skill }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MySkills',
  data() {
    return {
      name: 'Course in Vue',
      btnState: true,
      skills: [
        {"skill": "Vue.js"},
        {"skill": "Frontend Developer"}
      ]
    };
  },
  methods: {
    changeName() {
      this.name = 'New Name';
      this.btnState = !this.btnState;
    }
  }
};
</script>

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
