<template>
  <div class="weekend-item">
    <h2 class="weekend-title">周末去哪儿</h2>
    <div
        v-for="product of list"
        :key="product.id"
        class="weekend-product"
    >
      <a>
        <div class="product-img">
          <img :src="product.imgUrl" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">{{ product.name }}</p>
          <p class="product-desc">{{ product.desc }}</p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  .weekend-item
    .weekend-title
      height: .8rem
      padding-left: .26rem
      line-height: .8rem
      color: #212121
    .weekend-product
      background-color: #fff
      margin-bottom: .1rem
      a
        display: block
      .product-img
        width: 100%
        border-bottom: 37.21%
        img
          width: 100%
      .product-info
        padding: .14rem .2rem .2rem .2rem
        .product-name
          overflow: hidden
          padding-right: 1.4rem
          color: #212121
          font-size: .28rem
          line-height: .48rem
          white-space: nowrap
          text-overflow: ellipsis
        .product-desc
          overflow: hidden
          padding-right: 1.4rem
          color: #616161
          font-size: .24rem
          line-height: .42rem
          white-space: nowrap
          text-overflow: ellipsis
</style>
