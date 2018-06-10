<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe697;</span>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe6ac;</span>
      <span>输入城市/景点/游玩/主题</span>
    </div>

    <div class="header-right">
      <router-link to="/city">
      {{ city }}
      </router-link>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    display: flex
    height: $navHeight
    align-items: center
    background-color: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        headerBack()
    .header-input
      flex: 1
      height: .64rem
      line-height .64rem
      margin-left: .15rem
      color: #ccc
      background-color: #fff
      border-radius: .06rem
      .search-icon
        padding-left: .1rem
        font-size: .016rem
    .header-right
      height: 100%
      line-height: $navHeight
      padding: 0 .26rem
      color: #fff
      text-align: center
      a
        display: inline-block
        color: #fff
      &::after
         content: ''
         display: inline-block
         position: relative
         width: 1px
         top: .08rem
         border: 6px solid
         border-color: #fff transparent transparent
</style>
