<template>
  <div class="detail-page">
    <detail-header></detail-header>
    <detail-banner></detail-banner>
    <detail-base-info></detail-base-info>
    <detail-tciket-list></detail-tciket-list>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBanner from './components/Banner'
import DetailBaseInfo from './components/Baseinfo'
import DetailTciketList from './components/TciketList'
export default {
  name: 'Details',
  components: {
    DetailHeader,
    DetailBanner,
    DetailBaseInfo,
    DetailTciketList
  }
}
</script>

<style lang="stylus" scoped>
  .detail-page
    height: 20rem
    background-color: #f5f5f5
</style>
