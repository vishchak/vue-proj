<template>
  <div class="container">
    <h1 v-once>{{ name }}</h1>
    <button v-on:click="changeName" :disabled="btnState">Change name</button>
    {{ btnState ? 'The button is disabled' : 'The button is active' }}
    <div class="holder">
      <p>These are the skills that I possess</p>
      <ul>
        <li v-for="(data, index) in skills" :key="index">{{ index + 1 }}. {{ data.skill }}</li>
      </ul>
      <p v-if="skills.length >= 1">I have more than 1 skill</p>
      <p v-else>I have 1 or less skills :(</p>

      <input type="text" placeholder="Enter a skill you have..." v-model="skill">{{ skill }}
      <div v-bind:class="{alert: showAlert, 'another-class': showClass}"></div>

      <div v-bind:class="alertObject"></div>

      <div v-bind:style="{backgroundColor: bgColor, width: bgWidth, height: bgHeight}"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MySkills',
  data() {
    return {
      skill: '', // Fixed typo: Removed colon after v-model
      name: 'Course in Vue',
      btnState: true,
      skills: [
        {"skill": "Vue.js"},
        {"skill": "Frontend Developer"}
      ],
      showAlert: true,
      showClass: true,
      alertObject: {
        alert: true
      },
      bgColor: 'orange',
      bgWidth: '100%',
      bgHeight: '30px'
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
.alert {
  background-color: yellow;
  width: 100%;
  height: 30px;
}

.another-class {
  background-color: lightblue;
  width: 100%;
  height: 30px;
}

.holder {
  background: #fff;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

ul li {
  padding: 20px;
  font-size: 1.3em;
  background-color: #E0EDF4;
  border-left: 5px solid #3EB3F6;
  margin-bottom: 2px;
  color: #3E5252;
}

p {
  text-align: center;
  padding: 30px 0;
  color: grey;
}

.container {
  box-shadow: 0 0 40px lightgrey;
}


input {
  width: calc(100% - 40px);
  border: 0;
  padding: 20px;
  font-size: 1.3em;
  background-color: #323333;
  color: #687F7F;
}
</style>

