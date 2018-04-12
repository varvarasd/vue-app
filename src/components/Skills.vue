<template>
  <div class="skill">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'> {{index}}. {{data.skill}}</li>
      </ul>

      <div v-bind:class="{ alert: showAlert, 'class-name': showClass }"></div>
      <!-- use !showAlert for negative check-->
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
      ],
      showAlert: true,
      showClass: true
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .alert {
    background-color: red;
    width: 80%;
    height: 30px
  }

  .class-name {
    border: solid 10px blue;
  }

</style>
