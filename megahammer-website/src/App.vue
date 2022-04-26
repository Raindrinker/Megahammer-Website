<template>
  <div class="main">
    <PageHeader/>
    <div class="content">
      <div class="videosection">

        <div class="videosection-content">

          <div class="video-player" :class="{hidden: playerhidden}" ref="player">

            <vue-plyr ref="plyr">
              <div class="plyr__video-embed">
                <iframe
                    src="https://www.youtube.com/watch?v=1j9MdHglgck"
                    allowfullscreen
                    allowtransparency
                    allow="autoplay"
                ></iframe>
              </div>
            </vue-plyr>

          </div>
        </div>
      </div>

      <div class="contentsection">
        <div class="about">
          <div class="title">ABOUT</div>

          <div class="about-row">
            <div>
              <img src="./assets/vectormonke-transparency-badge.png" class="about-image">
            </div>
            <div class="text">
              Donovan Jonk is a multi-instrumentalist, composer, and sound designer. With a Bachelor of Music in jazz studies and music technology from Minnesota State University Moorhead, and a varied career in the music industry as a teacher, performer, freelance composer, and indie record label associate, Donovan comes with the experience and instincts to help your project find its unique sonic identity.
            </div>
          </div>


        </div>
      </div>

      <div class="bgsection">
        <div class="title">PROJECTS</div>

        <div class="project-list">
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
          <div class="project">
            <div class="project-inner">

            </div>
          </div>
        </div>
      </div>

      <div class="contentsection">
        <div class="title">CONTACT</div>
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
  components: {PageHeader},
  data() {
    return {
      playerhidden: true
    }
  },
  mounted() {
    this.$refs.plyr.player.on('ended', () => this.videoEnded())
  },
  methods: {
    onClickMonke() {
      this.playerhidden = false;
    },
    videoEnded() {
      this.$refs.plyr.player.restart();
      this.$refs.plyr.player.stop();
    }
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

  margin: 0;
  height: 100vh;
  width: 100%;

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

.logo-monke {
  max-width: 100%;
  position: absolute;

  z-index: 400;
}

.text {
  color: #AAAAAA;
  font-size: 24px;
}

.content {

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

  width: 100%;

  position: relative;
}

.videosection-content {

  padding: 32px;
  padding-top: 300px;


  position: relative;

  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.contentsection {
  width: 100%;

  background-color: #222222;

  min-height: 300px;

  color: #EEEEEE;

  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
}

.bgsection {

  min-height: 300px;

  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer {

  width: 100%;

  height: 150px;

  background-color: #050505;
}

.about {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title {
  color: white;
  font-size: 32px;
  padding-top: 32px;
}

.about .text {
  text-align: left;
  max-width: 800px;
}

.about-row {
  display: flex;
  align-items: center;

  padding-bottom: 64px;
}

.about-image {
  max-width: 300px;
}

.video-player {
  width: 100%;

  max-width: 1000px;

  transition: 0.5s;

  margin-top: -40px;

  border-radius: 16px;
  overflow: hidden;

  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
}

.project-list {
  display: flex;
  flex-wrap: wrap;

  align-items: center;
  justify-content: center;

  max-width: 80%;

  padding-bottom: 64px;
  padding-top: 32px;
}

.project {

  padding: 32px;
}

.project-inner {
  background-color: #111111;
  width: 300px;
  height: 250px;

  border-radius: 16px;
  overflow: hidden;

  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
}

</style>
