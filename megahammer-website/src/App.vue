<template>
  <div class="main">
    <img src="./assets/vectormonke.png" class="logo">
    <div class="text">UNDER CONSTRUCTION</div>
  </div>
</template>

<script>

export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  margin: 0;
  height: 100vh;
  overflow: hidden;

  display: flex;
  flex-direction: column;
}

body {
  margin: 0;
  background-color: black;
}

.main {
  flex-grow: 1;

  display: flex;
  flex-direction: column;
  align-items: center;

  padding-top: 128px;
}

.logo {
  max-width: 30%;
}

.text {
  color: #AAAAAA;
  font-size: 24px;
}
</style>
