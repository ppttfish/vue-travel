<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-nav :list="navList"></home-nav>
    <home-recommend :list="recommendList"></home-recommend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeNav from './components/Nav'
import HomeRecommend from './components/Recommend'
import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
      city: '',
      swiperList: [],
      navList: [],
      recommendList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeNav,
    HomeRecommend
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.logInfo)
    },
    logInfo (res) {
      res = res.data
      this.city = res.data.city
      this.swiperList = res.data.swiperList
      this.navList = res.data.navList
      this.recommendList = res.data.recommendList
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
