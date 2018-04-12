<template>
  <div class="skill">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'> {{index}}. {{data.skill}}</li>
      </ul>

      <p v-if="skills.length >= 1"> You have more than 1 skills</p>
      <p v-else>You have less than 1 skills</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return{
      skills:[
        {'skill': 'Vue.js'},
        {'skill': 'Frontend Dev'}
      ]
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./skills.css" scoped>

</style>
