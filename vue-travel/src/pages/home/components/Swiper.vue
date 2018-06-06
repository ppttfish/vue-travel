<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="isShow">
      <!-- slides -->
      <swiper-slide v-for="item in list" :key="item.id">
        <img  class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true,
        autoplay: true
      }
    }
  },
  computed: {
    isShow () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
    opacity: .7 !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 56.26%
    background-color: #ccc
    .swiper-img
      width: 100%
</style>
