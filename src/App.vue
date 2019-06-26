<template>
  <div id="app">
    <b-container fluid>
      <b-row>
        <b-col md="8" lg="8" class="grid-charcoal"></b-col>
        <b-col md="4" lg="4" class="grid-light-gray"></b-col>
      </b-row>
      <b-row>
        <b-col md="6" lg="6" class="grid-light-gray"></b-col>
        <b-col md="6" lg="6" class="grid-gray"></b-col>
      </b-row>
    </b-container>
    <pictureGridContainer v-bind:pictures="pictures" />
  </div>
</template>

<script>
import pictureGridContainer from './components/picture-grid-container.vue'

const PexelsAPI = require('pexels-api-wrapper');
var pexelsClient = new PexelsAPI("563492ad6f91700001000001fb92b9f45c564ef6a4953c94c1ddbd98");

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
    pexelsClient.search("dog", 1, Math.floor(Math.random() * 1000) + 1)
    .then(res => this.pictures = res.photos)
    .catch(err => console.log(err));
  }
}
</script>

<style>
#app {
  background-color: #7EC7EE;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.grid-charcoal{
  background: #333;
  min-height: 55vh;
}

.grid-light-gray{
  background: #CFCFCF;
  min-height: 55vh;
}

.grid-gray{
  min-height: 45vh;
  background: #BDBDBD;
}
</style>
