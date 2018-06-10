<template>
  <div class="my-page">
    <home-header :city="this.$store.state.city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-nav :list="navList"></home-nav>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeNav from './components/Nav'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
      swiperList: [],
      navList: [],
      recommendList: [],
      weekendList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeNav,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.logInfo)
    },
    logInfo (res) {
      res = res.data
      this.swiperList = res.data.swiperList
      this.navList = res.data.navList
      this.recommendList = res.data.recommendList
      this.weekendList = res.data.weekendList
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style lang="stylus" scope>
  .my-page
    background-color: #f5f5f5
</style>
