<template>
  <div class="detial-order">
    <div class="order-wrapper">
      <div class="order-info">
        <h5 class="order-title">华清宫（华清池·骊山）成人门票 景区官方直营</h5>
        <p class="order-price">
          <span class="price-icon">￥<em class="price-num">135</em></span>
          <span>/张</span>
        </p>
      </div>
      <div class="order-select">
        <h6 class="order-note">价格日历</h6>
        <div class="order-datecards">
          <span class="order-datecard order-datecard-disabled">
            <em class="date-name">今天</em>
            <strong class="date-detial">6月11日</strong>
          </span>
          <span class="order-datecard order-datecard-active">
            <em class="date-name">明天</em>
            <strong class="date-detial">6月11日</strong>
          </span>
          <span class="order-datecard">
            <em class="date-name">后天</em>
            <strong class="date-detial">6月11日</strong>
          </span>
          <span class="order-datecard">
            <em class="date-name">其他日期</em>
            <strong class="date-detial"></strong>
          </span>
        </div>
      </div>
      <div class="order-tips">需要在游玩当天的00:00前预订</div>
    </div>
    <div class="order-btn">立即预定</div>
    <div  @click="handleOrderClick" class="order-close iconfont">&#xe603;</div>
  </div>
</template>

<script>
export default {
  name: 'DetailOrder',
  methods: {
    handleOrderClick () {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .detial-order
    position: fixed
    z-index: 1
    top: 8.3rem
    left: 0
    right: 0
    bottom: 0
    background-color: #fff
    .order-wrapper
      margin: 0 .2rem
      .order-info
        .order-title
          margin-right: .6rem
          padding: .3rem 0 .1rem
          color: #212121
          font-size: .34rem
          line-height: .4rem
        .order-price
          color: #9e9e9e
          font-size: .24rem
          line-height: .48rem
          .price-icon
            color: #ff9800
            margin-right: .06rem
            .price-num
              margin-left: .06rem
              font-size: .36rem
      .order-select
        margin-top: .18rem
        .order-note
          color: #333;
          font-size: .26rem
          line-height: .65rem
        .order-datecards
          height: .86rem
          .order-datecard:first-child
            margin-left: 0
          .order-datecard:last-child
            .date-name
              line-height: .65rem
          .order-datecard
            box-sizing: border-box
            float: left
            width: 22.5%
            height: .86rem
            margin-left: 3.33%
            border: 1px solid #bdbdbd
            border-radius: .08rem
            .date-name
            .date-detial
              display: block
              text-align: center
            .date-name
              padding-top: .08rem
              color: #212121
              font-size: .28rem
              line-height: .36rem
            .date-detial
              padding-bottom: .06rem
              color: #888
              font-size: .24rem
              line-height: .32rem
          .order-datecard-active
            position: relative
            border: 1px solid #00bcd4
            color: #fff
            background: #00bcd4
            &::after
              content: '√'
              display: block
              position: absolute
              right: 0
              bottom: 0
              color: #fff
              speak: none
              font-size: .32rem
              line-height: 1
              font-smoothing: antialiased
            .date-name
            .date-detial
              color: #fff
          .order-datecard-disabled
            border-color: #ececec
            background: #fff
            .date-name
            .date-detial
              color: #ececec
      .order-tips
        padding: .14rem 0
        color: #ff8300
        font-size: .24rem
        line-height: .36rem
    .order-btn
      display: block
      border: 0 none
      background: #ff9800
      color: #fff
      font: normal .36rem/1rem Arial,"Microsoft Yahei","Helvetica Neue",Helvetica,sans-serif
      text-align: center
    .order-close
      position: absolute
      top: 0
      right: 0
      width: .88rem
      height: 1rem
      color: #9e9e9e
      font-size: .4rem
      line-height: 1rem
      text-align: center
</style>
