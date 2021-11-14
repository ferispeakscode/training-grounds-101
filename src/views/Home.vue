<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <BasicForm type="A"/>
    <BasicForm type="B"/>
    <BasicForm type="C"/>
  </div>
</template>

<script>
// @ is an alias to /src
import BasicForm from '@/components/BasicForm.vue'

export default {
  name: 'App',
  components: {
    BasicForm
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
