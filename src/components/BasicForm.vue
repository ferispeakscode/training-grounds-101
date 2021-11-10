<template>
  <h1>Basic form with configuration {{ config }} will go here.</h1>
</template>

<script>
export default {
  name: 'BasicForm',
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
