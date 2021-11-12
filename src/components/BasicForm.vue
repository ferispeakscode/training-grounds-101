<template>
  <h1>Basic form with configuration {{ config }} will go here.</h1>
  <form>
    <label>Name</label>
    <input type="text" v-model="user">
    <label>Gender</label>
    <select v-model="sex">
      <option value="Male">Male</option>
      <option value="Female">Female</option>
      <option value="Confused">Other</option>
    </select>
    <label>Age</label>
    <input type="number" size="100" min="1" max="100" step="1" v-model="age">
    <button>Submit</button>
    <button>Delete</button>
  </form>
  
  <p>{{user}}</p>
  <p>{{sex}}</p>
  <p>{{age}}</p>
</template>

<script>
export default {
  name: 'BasicForm',
  data() {
    return{
      user: '',
      sex: 'select',
      age: null
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
input, select {
  border: none;
  border-bottom: solid;
  }
label {
  text-transform: uppercase;
  display: inline-block;
}
form {
  width: 420px;
}
button {
  background: grey;
}
button:hover {
  background: rgb(58, 250, 186);
}
</style>
