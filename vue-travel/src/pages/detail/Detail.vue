<template>
  <div>
    <detail-banner></detail-banner>
    <detail-base-info></detail-base-info>
    <detail-tciket-list></detail-tciket-list>
  </div>
</template>

<script>
import DetailBanner from './components/banner'
import DetailBaseInfo from './components/baseinfo'
import DetailTciketList from './components/tciketList'
export default {
  name: 'Details',
  components: {
    DetailBanner,
    DetailBaseInfo,
    DetailTciketList
  }
}
</script>

<style lang="stylus" scoped>
  div
    background-color: #f5f5f5
</style>
