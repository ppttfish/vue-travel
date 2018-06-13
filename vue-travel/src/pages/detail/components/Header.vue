<template>
  <div
      class="detial-head"
      :style="opacityStyle"
      v-show="showHead"
  >
    <router-link
              class="nav-left"
              to="/"
              tag="div"
    >
      <span class="iconfont back">&#xe697;</span>
    </router-link>
    <h1 class="detial-title">{{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  props: {
    name: String
  },
  data () {
    return {
      showHead: false,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 30) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showHead = true
      } else {
        this.showHead = false
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
    .detial-head
      position: fixed
      width: 100%
      height: $navHeight
      background-color: $bgColor
      z-index: 1
      .nav-left
        position: absolute
        .back
          display: block
          width: .8rem
          line-height: $navHeight
          color: #fff
          font-size: .6rem
          text-align: center
      .detial-title
        display: block
        height: $navHeight
        line-height: $navHeight
        text-align: center
        color: #fff
        font-size: .32rem
</style>
