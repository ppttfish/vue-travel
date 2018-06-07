<template>
  <div class="map-tab">
    <ul>
      <li class="active">境内</li>
      <li>境外·港澳台</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CityTab'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .map-tab
    height: .4rem
    line-height: .4rem
    background-color: $bgColor
    padding: .2rem 1rem
    ul
      border: 1px solid #fff
      color: #fff
      overflow: hidden
      .active
        color: $bgColor
        background-color: #fff
      li
        display: inline-block
        width: 50%
        float: left
        text-align: center
</style>
