<template>
  <div class="city-head">
      城市
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
    height: $navHeight
    line-height: $navHeight
    background: $bgColor
    color: #fff
    text-align: center
    .header-left
      position: absolute
      color: #fff
      top: 0
      .city-back
        headerBack()
</style>
