<template>
  <div class="item-banner">
    <div @click="handleBannerClick" class="img-wrapper">
      <img :src="bannerImgUrl" alt="">
    </div>
    <div class="banner-info">
      <div class="banner-title">{{ name }}</div>
    </div>
    <div class="banner-img-icon">
      <span class="iconfont">&#xe61d;</span>
      <em class="img-num">34</em>
    </div>
    <router-link
                class="banner-back"
                to="/"
    >
      <span class="iconfont">&#xe697;</span>
    </router-link>
    <common-gallery
                  @back="handleGlalleryClose"
                  v-show="showGallery"
    >
    </common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery'
export default {
  name: 'DetailBanner',
  props: {
    name: String,
    bannerImgUrl: String
  },
  components: {
    CommonGallery
  },
  data () {
    return {
      showGallery: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGlalleryClose () {
      this.showGallery = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .item-banner
    position: relative
    &::after
        content: ''
        display: block
        position: absolute
        width: 100%
        height: .6rem
        bottom: 0
        left: 0
        background: linear-gradient(to bottom,rgba(0,0,0,0),rgba(0,0,0,.8))
    .img-wrapper
      overflow: hidden
      height: 0
      padding-bottom: 55%
      background-color: #ccc
      img
        width: 100%
    .banner-info
      position: absolute
      left: .2rem
      right: .2rem
      bottom: .36rem
      min-height: .4rem
      .banner-title
        line-height: .4rem;
        color: #fff;
        font-size: .36rem;
        text-shadow: 0 1px 2px rgba(0,0,0,0.70);
    .banner-img-icon
      position: absolute
      width: 1.2rem;
      height: .4rem;
      background: rgba(0,0,0,.5);
      border-radius: .2rem;
      left: .2rem
      bottom: .86rem
      font-size: .24rem
      color: #fff
      text-align: center
    .banner-back
      position: absolute
      margin: .1rem
      padding: .1rem
      top: 0
      background-color: rgba(0, 0, 0, .5)
      border-radius: .36rem
      span
        color: #fff
        font-size:.52rem
        font-weight: 600
</style>
