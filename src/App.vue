<template>
  <div id="app">
    <Login/>
  </div>
</template>

<script>
import Login from "./components/Login"

export default {
  name: 'App',
  components: {
    Login
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
}

* {
  box-sizing: border-box;
  
}

body {
  margin: 0;
  padding: 0;
  background: url("wallhaven-4gjvrd.jpg") center center no-repeat;
  background-size: cover;
  background-attachment: fixed;
}

</style>
