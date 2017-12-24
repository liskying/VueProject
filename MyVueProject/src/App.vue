<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <hello></hello>
    <message></message>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Message from './components/Message'

export default {
  components: {
    Hello,
    Message
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -200px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
