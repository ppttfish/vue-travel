<template>
  <div>
    <city-header></city-header>
    <city-tab @change="handleCityChange"></city-tab>
    <city-list :cityData="cityDomesticData" v-show="isDomesticShow"></city-list>
    <city-list :cityData="cityForiegnData" v-show="!isDomesticShow"></city-list>
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
      cityDomesticData: {},
      cityForiegnData: {},
      showCityList: '',
      isDomesticShow: true
    }
  },
  components: {
    CityHeader,
    CityTab,
    CityList
  },
  methods: {
    getDomesticCityInfo () {
      axios.get('/api/city.json')
        .then(this.logDomesticInfo)
    },
    getForiegnCityInfo () {
      axios.get('/api/foriegn.json')
        .then(this.logForiegnInfo)
    },
    logDomesticInfo (res) {
      res = res.data
      this.cityDomesticData = res.data
    },
    logForiegnInfo (res) {
      res = res.data
      this.cityForiegnData = res.data
    },
    handleCityChange (isDometicShow) {
      this.isDomesticShow = isDometicShow
    }
  },
  mounted () {
    this.getDomesticCityInfo()
    this.getForiegnCityInfo()
  }
}
</script>

<style>

</style>
