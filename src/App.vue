<template>
  <div id="app">
    <HeaderComponent @search="makeResearch" />
    <MainComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'

import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    
  },
  data(){
    return{
      apiUrl: 'https://api.themoviedb.org/3/search/',
      apiKey: 'd390a548a1b367f9298f733e846c5f99',
    }
  },
  methods:{
    makeResearch(searchFilm){
      console.log(searchFilm);
      const params = {
        api_key: this.apiKey,
        query: searchFilm,

      }
      axios.get(this.apiUrl + 'movie', {params}).then((response)=>{
        console.log(response);
      }).catch(error=>{
        console.log(error)
      });

    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
