<template>
  <div class="city-head boder-bottom">
      城市选择
    <router-link to="/">
      <div class="header-left">
        <span class="iconfont city-back">&#xe697;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .city-head
    position: relative
    height: .68rem
    line-height: .88rem
    background: $bgColor
    color: #fff
    text-align: center
    font-size: .32rem
    .header-left
      position: absolute
      color: #fff
      top: 0
      .city-back
        headerBack()
</style>
