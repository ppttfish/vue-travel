<template>
  <div class="home-recommend">
    <div class="recommend-title">
      <img  class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
      <span class="rmd-title">猜你喜欢</span>
    </div>
    <ul v-for="item of list" :key="item.id" class="recommend-block border-bottom">
      <router-link
                  class="recommend-item"
                  tag="li"
                  :to="'/detail/' + item.id"
      >
        <div class="item-img">
          <img :src="item.imgUrl" alt="">
          <div class="img-exra">可订明日</div>
        </div>
        <div class="item-info">
          <div class="item-info-title">{{ item.name }}</div>
          <div class="item-commit">
            <span class="iconfont commit-start">&#xe7f1;&#xe7f1;&#xe7f1;&#xe7f1;</span>
            <span class="commit-num">{{ item.commit }}条评论</span>
          </div>
          <div class="item-price">
            <span class="real-price">￥<em>{{ item.price }}</em></span>
            起
            <span class="item-address">{{ item.address }}</span>
          </div>
        </div>
      </router-link>
    </ul>
    <a class="more-items">查看所有产品</a>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .home-recommend
    margin-top: .2rem
    background-color: #fff
    .recommend-title
      padding: .24rem 0 .26rem
      .title-img
        display: inline-block
        width: .3rem
        height: .3rem
        margin-left: .2rem
        vertical-align: top
      .rmd-title
        display: inline-block
        height: .44rem
        color: #212121
        font-size: .32rem
        line-height: .44rem
    .recommend-block
      display: block
      box-sizing: border-box
      margin-left : .24rem
      color: black
      .recommend-item
        overflow hidden
        padding: .2rem 0
        .item-img
          float: left
          overflow: hidden
          width: 2rem
          height: 2rem
          img
            width: 100%
          .img-exra
            position: absolute
            box-sizing: border-box
            top: .2rem
            padding: .05rem
            font-size: .2rem
            background-color: #01CDE7
            color: #fff
        .item-info
          overflow: hidden
          padding-left: .22rem
          .item-info-title
            margin-top: .26rem
            height: .44rem
            color: #212121
            font-size: .32rem
            line-height: .44rem
          .item-commit
            margin-top: .14rem
            height: .34rem
            .commit-start
              color: #ffb436
              font-size: .24rem
              line-height: .34rem
            .commit-num
              color: #616161
              font-size: .24rem
              line-height: .26rem
              margin-left: .2rem
              vertical-align: text-bottom
          .item-price
            position: relative
            margin-top: .22rem
            color: #616161
            font-size: .24rem
            line-height: .4rem
            .real-price
              color: #ff8300
            em
              font-size: .4rem
            .item-address
              position: absolute
              right: .24rem
              bottom: 0
  .more-items
    display: block;
    padding: .2rem 0;
    color: #00afc7;
    font-size: .28rem;
    line-height: .4rem;
    text-align: center;
</style>
