<template>
  <div id="app">
    <Header class="container" />
    <Main :albumsMusic="albumsMusic" />
  </div>
</template>

<script>
import axios from 'axios';
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return{
      albumsMusic: []
    }
  },
  created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result)=> {
      this.albumsMusic = result.data.response
    })
  }
}
</script>

<style lang="scss">

  @import "./style/app.scss";

</style>
