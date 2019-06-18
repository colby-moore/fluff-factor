<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <pictureGridContainer v-bind:pictures="pictures" />
  </div>
</template>

<script>
import pictureGridContainer from './components/picture-grid-container.vue'

const PexelsAPI = require('pexels-api-wrapper');
var pexelsClient = new PexelsAPI("");

export default {
  name: 'app',
  components: {
    pictureGridContainer
  },
  data() {
    return{
      pictures: []
    }
  },
  created(){
    pexelsClient.search("dog", 3, 1)
    .then(res => this.pictures = res.photos)
    .catch(err => console.log(err));
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
