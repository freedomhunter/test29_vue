<template>
  <div class="hello">
    <video autoplay muted loop id="myVideo">
    <source src="../assets/dash.mp4" type="video/mp4">
      Your browser does not support HTML5 video.
    </video>
    <div class="baseCard">
      <MiddleDash />
      <hr>
      <Navigation />
    </div>
  </div>
</template>

<script>
import Navigation from './Navigation';
import MiddleDash from './MiddleDash';

export default {
  name: 'Main',
  components:{
    MiddleDash,
    Navigation
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.baseCard{
  border-radius:5px;
  padding: 2%;
  width: 50%;
  margin: auto;
  margin-top: 10%;
  background-color: black;
  opacity: 0.85;
  box-shadow: 0px 0px 25px black;
}
#myVideo {
  position: fixed;
  filter: blur(0px);
  right: 0;
  bottom: 0;
  min-width: 100%; 
  min-height: 100%;
  z-index: -1;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
