<template>
  <div class="detail-page">
    <detail-header></detail-header>
    <detail-banner></detail-banner>
    <detail-base-info></detail-base-info>
    <detail-tciket-list @buy="handleBuyBtn"></detail-tciket-list>
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
      showMask: false
    }
  },
  methods: {
    handleOrderClose () {
      this.showOrder = this.showMask = false
    },
    handleBuyBtn () {
      this.showOrder = this.showMask = true
    }
  }
}
</script>

<style lang="stylus" scoped>
  .detail-page
    height: 20rem
    background-color: #f5f5f5
</style>
