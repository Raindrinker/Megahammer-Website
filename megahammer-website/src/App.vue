<template>
  <div class="main">
    <PageHeader/>
    <div class="content">
      <div class="videosection">

        <div class="videosection-content">

          <img src="./assets/vectormonke-transparency-badge.png" class="logo">
        </div>
      </div>

      <div class="contentsection">

      </div>

      <div class="bgsection">

      </div>

      <div class="contentsection">

      </div>

      <div class="footer">

      </div>

    </div>
  </div>
</template>

<script>

import PageHeader from "@/components/PageHeader";
export default {
  name: 'App',
  components: {PageHeader}
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
  width: 100vw;

  display: flex;
  flex-direction: column;
}

body {
  margin: 0;
  background-color: black;
}

.main {

  width: 100%;

  display: flex;
  flex-direction: column;

}

.logo {
  max-width: 100%;
}

.text {
  color: #AAAAAA;
  font-size: 24px;
}

.content {

  width: 100%;

  display: flex;

  flex-direction: column;

  align-items: center;
  justify-content: center;

  flex-shrink: 0;

  background-image: url("./assets/hammerpattern.png");
  background-attachment: fixed;
  background-position: center;
  background-repeat: repeat;
  background-size: 100px;

}

.videosection {

  height: 100vh;
}

.videosection-content {
  padding-top: 250px;
}

.contentsection {
  width: 100%;

  background-color: #333333;

  height: 300px;
}

.bgsection {

  height: 300px;
}

.footer {

  width: 100%;

  height: 150px;

  background-color: #050505;
}
</style>
