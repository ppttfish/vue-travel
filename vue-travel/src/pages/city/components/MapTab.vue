<template>
  <div class="map-tab">
    <ul @click="isShow">
      <li :class="{ active: isDomesticActive }" id="domestic">境内</li>
      <li :class="{ active: !isDomesticActive }" id="foreign">境外·港澳台</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CityTab',
  data () {
    return {
      isDomesticActive: true
    }
  },
  methods: {
    isShow (e) {
      const ele = e.target
      if (ele.id === 'domestic') {
        this.isDomesticActive = true
        this.$emit('change', true)
      } else {
        this.isDomesticActive = false
        this.$emit('change', false)
      }
    }
  }
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
