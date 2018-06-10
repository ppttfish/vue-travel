<template>
  <div class="gallery">
    <div class="gallery-header border-bottom">
      <div  @click="hanldBackClick" class="nav-left">
        <span class="iconfont gallery-back">&#xe697;</span>
      </div>
      <h1 class="gallery-title">景区图片</h1>
    </div>
    <div class="img-list">
      <div
          v-for="(img, index) of smallImgList"
          :key="index"
          class="img-wrapper"
          @click="handleGalleryClick(index)"
      >
        <img  class="imgs" :src="img" alt="">
      </div>
    </div>
    <div  @click="handleGalleryClick" class="img-show" v-show="showGallery">
      <div class="wrapper">
        <swiper :options="swiperOption">
          <!-- slides -->
          <swiper-slide v-for="(img, index) of realImgList" :key="index">
            <img  class="swiper-img"  alt="" :src="img">
          </swiper-slide>
          <!-- Optional controls -->
          <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
  methods: {
    hanldBackClick () {
      this.$emit('back')
    },
    handleGalleryClick (index) {
      this.showGallery = !this.showGallery
    }
  },
  data () {
    return {
      showGallery: false,
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        observeParents: true,
        observe: true,
        autoplay: true,
        initialSlide: 0
      },
      smallImgList: [
        'http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_350x240_a9a78d86.jpg',
        'http://img1.qunarzz.com/sight/p0/1706/73/7349ea5c85af9d5ea3.img.png_350x240_c428674e.png',
        'http://img1.qunarzz.com/sight/p0/1706/4d/4dc144af8b342ad2a3.img.png_350x240_a57d67cc.png',
        'http://img1.qunarzz.com/sight/p0/1706/30/30b75fe5792c3e59a3.img.png_350x240_01270bb3.png',
        'http://img1.qunarzz.com/sight/p0/1706/12/12537e17721ff9c0a3.img.png_350x240_e794e531.png',
        'http://img1.qunarzz.com/sight/p0/1706/4c/4cd7dd2b4c0ee33ca3.img.png_350x240_5265d4a1.png'
      ],
      realImgList: [
        'http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_r_800x800_743eaecf.jpg',
        'http://img1.qunarzz.com/sight/p0/1706/73/7349ea5c85af9d5ea3.img.png_r_800x800_2afd15e0.png',
        'http://img1.qunarzz.com/sight/p0/1706/4d/4dc144af8b342ad2a3.img.png_r_800x800_740c4665.png',
        'http://img1.qunarzz.com/sight/p0/1706/30/30b75fe5792c3e59a3.img.png_r_800x800_3c5ac04b.png',
        'http://img1.qunarzz.com/sight/p0/1706/12/12537e17721ff9c0a3.img.png_r_800x800_c4529145.png',
        'http://img1.qunarzz.com/sight/p0/1706/4c/4cd7dd2b4c0ee33ca3.img.png_r_800x800_f9819c21.png'
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .gallery >>> .swiper-pagination
    position: absolute
    color: #fff
    font-size: .2rem
    bottom: -3.8rem
  .gallery >>> .swiper-container
    overflow: inherit
  .gallery
    position: fixed
    top: 0
    left: 0
    right: 0
    bottom: 0
    background-color: #f5f5f5
    z-index: 1
    .gallery-header
      position: fixed
      width: 100%
      height: $navHeight
      background-color: #fff
      .nav-left
        position: absolute
        .gallery-back
          display: block
          width: .8rem
          line-height: $navHeight
          font-size: .6rem
          text-align: center
      .gallery-title
        display: block
        height: $navHeight
        line-height: $navHeight
        text-align: center
        font-size: .32rem
    .img-list
      overflow: hidden
      width: 100%
      box-sizing: border-box
      padding: $navHeight + .2rem .2rem 0 .2rem
      .img-wrapper:nth-child(odd)
        padding-right: .05rem
      .img-wrapper
        float: left
        box-sizing: border-box
        width: 50%
        margin-bottom: .1rem
        img
          width: 100%
    .img-show
      display: flex
      position: absolute
      align-items: center
      top: 0
      left: 0
      right: 0
      bottom: 0
      background-color: black
      .wrapper
        width: 100%
        height: 0
        padding-bottom: 56.8%
        .swiper-img
          width: 100%
</style>
