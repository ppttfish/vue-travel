<template>
  <div>
    <city-header></city-header>
    <city-tab></city-tab>
    <city-list :cityData="cityData"></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CityTab from './components/MapTab'
import CityList from './components/CityList'
import axios from 'axios'
export default {
  name: 'City',
  data () {
    return {
      cityData: {}
    }
  },
  components: {
    CityHeader,
    CityTab,
    CityList
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.logInfo)
    },
    logInfo (res) {
      res = res.data
      this.cityData = res.data
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style>

</style>
