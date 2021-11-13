<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <BasicForm type="A"/>
    <BasicForm type="B"/>
    <BasicForm type="C"/>
    <HelloWorld msg="Welcome to Training Grounds 101"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import BasicForm from '@/components/BasicForm.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
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
