<template>
  <div class="detail-page">
    <detail-header :name="name"></detail-header>
    <detail-banner :bannerImgUrl="bannerImgUrl" :name="name"></detail-banner>
    <detail-base-info :baseInfo="this.baseInfo"></detail-base-info>
    <detail-tciket-list :list="this.ticketsList" @buy="handleBuyBtn"></detail-tciket-list>
    <detail-order @close="handleOrderClose" v-show="showOrder"></detail-order>
    <detail-mask @maskClick="handleOrderClose" v-show="showMask"></detail-mask>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBanner from './components/Banner'
import DetailBaseInfo from './components/Baseinfo'
import DetailTciketList from './components/TciketList'
import DetailOrder from './components/Order'
import DetailMask from 'common/mask'
import axios from 'axios'
export default {
  name: 'Details',
  components: {
    DetailHeader,
    DetailBanner,
    DetailBaseInfo,
    DetailTciketList,
    DetailOrder,
    DetailMask
  },
  data () {
    return {
      showOrder: false,
      showMask: false,
      baseInfo: {},
      ticketsList: [],
      name: '',
      bannerImgUrl: ''
    }
  },
  methods: {
    handleOrderClose () {
      this.showOrder = this.showMask = false
    },
    handleBuyBtn () {
      this.showOrder = this.showMask = true
    },
    getDetailInfo () {
      axios.get('/api/detail.json')
        .then(this.logInfo)
    },
    logInfo (res) {
      let id = this.$route.params.id.substring(2) - 1
      console.log(id)
      res = res.data
      this.baseInfo = res.data.itemList[id].commitList
      this.ticketsList = res.data.itemList[id].ticketsList
      this.name = res.data.itemList[id].name
      this.bannerImgUrl = res.data.itemList[id].bannerImgUrl
    }
  },
  mounted () {
    this.getDetailInfo()
  }
}
</script>

<style lang="stylus" scoped>
  .detail-page
    height: 20rem
    background-color: #f5f5f5
</style>
