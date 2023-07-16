<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Navbar></Navbar>
  <Form></Form>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue';
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Form
    //HelloWorld
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
