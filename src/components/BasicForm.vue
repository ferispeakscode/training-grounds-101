<template>
  <h1>Basic form with configuration {{ config }} will go here.</h1>
  <label>Name</label>
  <input type="text" v-model="user">
  <p>{{user}}</p>
</template>

<script>
export default {
  name: 'BasicForm',
  data() {
    return{
      user: ''
    }
  },
  props: {
    config: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
    color: red;
}
</style>
