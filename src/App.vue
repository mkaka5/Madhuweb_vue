<template>
  <div class="container">
    <WebSeriesHeader/>
    <WebSeriesList :webSeriesData = webSeriesData />
</div>
</template>

<script>

import WebSeriesHeader from './components/WebSeriesHeader.vue'
import WebSeriesList from './components/WebSeriesList.vue'

export default {
  name: 'App',
  components: {    
    WebSeriesHeader,
    WebSeriesList
  },

  data(){
    return {
      webSeriesData: []
    }

  },

  methods: {
    // promises
    async fetchWebSeries(){
      const res = await fetch('https://webseries-cod4.onrender.com/api')
      const data = await res.json();
      console.log(data[0].webseries);
      return data[0].webseries;
    }
  },
  async created(){
    this.webSeriesData = await this.fetchWebSeries();
  }
}
</script>

<style>

</style>
