<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
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
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      list: [
        {
          id: '0001',
          imgUrl: '/static/img/swiper1.jpeg'
        },
        {
          id: '0002',
          imgUrl: '/static/img/swiper2.jpeg'
        },
        {
          id: '0003',
          imgUrl: '/static/img/swiper3.jpeg'
        }
      ]
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
    .swiper-img
      width: 100%
</style>
