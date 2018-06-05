<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe697;</span>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe6ac;</span>
      输入城市/景点/游玩/主题
    </div>
    <div class="header-right">
      城市
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    display: flex
    height: .86rem
    align-items: center
    background-color: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        margin-left: .1rem
        font-size: .5rem
    .header-input
      flex: 1
      height: .64rem
      line-height .64rem
      margin-left: .2rem
      color: #ccc
      background-color: #fff
      border-radius: .1rem
      .search-icon
        padding-left: .1rem
        font-size: .016rem
    .header-right
      float: right
      width: 1.5rem
      text-align: center
      margin-left: -.3rem
      &::after
         content: ''
         display: block
         position: absolute
         width: 1px
         right: .18rem
         top: .38rem
         border: 6px solid
         border-color: #fff transparent transparent
</style>
