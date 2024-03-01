<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'


window.onload = function() {
  window.addEventListener('scroll', playAudio);
  window.addEventListener('click', playAudio);
  window.addEventListener('mousedown', playAudio);
  window.addEventListener('touchstart', playAudio);
};

function playAudio() {
  var audio = document.getElementById('audioplayback');
  if ((<any>audio).paused) {
    (<any>audio).volume = 0.1;
    (<any>audio).currentTime = 17.5;
    (<any>audio).play();
  }
}

</script>

<template>
  <audio id="audioplayback" src="/videoplayback.m4a" type="audio/mp4"></audio>
  <div class="background-container"><img id="background-video" src="/noah-rockstar-made.gif"></div>
  <div class="container">
    <h1>Даугавпилс</h1>
    <h3>Наш Дискорд</h3>
    <a href="https://discord.com/invite/9ZFNmPXWRn">discord.me</a>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

.container {
  font-family: 'Poppins', sans-serif;
  /* font-weight: bold; */
  
  height: 100%;
  pointer-events: none;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  z-index: 1;

  text-align: center;
  line-height: 2rem;
  font-size: 18px;
  color: #fff;
}

a {
  color: #fff;
  pointer-events: all;
  margin-top: 1rem;
  letter-spacing: 5px;
}

a:after {
  color: #fff;
}

.welcome-block {
  width: 45%;
}

.background-container {
  pointer-events: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  opacity: 0.2;
  z-index: -1;
}

#background-video {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

</style>
