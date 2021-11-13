<template>
  <h1>Basic form with configuration {{ config }} will go here.</h1>
  <form @submit.prevent="submitData">
    <label>Surname</label>
    <input type="text" v-model="surname">
    <label>Firstname</label>
    <input type="text" v-model="fname">
    <label>Gender</label>
    <select v-model="sex">
      <option value="Male">Male</option>
      <option value="Female">Female</option>
    </select>
    <label>Age</label>
    <input type="number" size="100" min="1" max="100" step="1" v-model="age">
    <button>Submit</button>
    <button>Delete</button>
  </form>
  
  <p>{{fname}} {{surname}}</p>
  <p>{{sex}}</p>
  <p>{{age}}</p>
</template>

<script>
export default {
  name: 'BasicForm',
  data() {
    return{
      surname: '',
      fname: '',
      sex: 'select',
      age: null,
      uri: 'http://localhost:3000/Information'
    }
  },
  props: {
    config: String
  },
  methods: {
    submitData(){
      let personalData = {
        surname: this.surname,
        fname: this.fname,
        sex: this.sex,
        age: this.age
      }
      fetch('http://localhost:3000/Information', {
        method: 'POST',
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify(personalData)
      })
    }
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
  border-bottom: 1px solid #ddd;
  box-sizing: border-box;
  color: #555;
  padding: 10px 6px;
  width: 100%;
  }
label {
  text-transform: uppercase;
  display: inline-block;
  font-size: .8em;
  color: #aaa;
}
form {
  max-width: 680px;
  padding: 40px;
  margin: 25px 0 15px;
  display: inline-block;
  font-size: 0.8em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
button {
  background: grey;
  color:#ddd;
  padding: 8px 18px;
  margin: 15px 5px;
  border: none;
}
button:hover {
  background: rgb(58, 250, 186);
}
</style>
