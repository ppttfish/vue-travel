<template>
  <div class="tciketList">
    <h3 class="tk-title border-bottom">去哪儿推荐</h3>
    <div class="tk-item border-top">
      <div class="tk-info">
        <h3 class="tk-title">【随买随用】《长恨歌》第一场中区</h3>
        <span class="tk-tips">
          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" alt="">
          可订明日
        </span>
        <div class="tk-exra">
          <span class="border">
            <img src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
            自营
          </span>
          <span class="border">条件退</span>
        </div>
      </div>
      <div class="tk-btn">
        <div class="tk-price">￥<em>298</em></div>
        <div class="tk-buy-btn">预定</div>
      </div>
    </div>
    <div class="tk-item border-top">
      <div class="tk-info">
        <h3 class="tk-title">【随买随用】《长恨歌》第一场中区</h3>
        <span class="tk-tips">
          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" alt="">
          可订明日
        </span>
        <div class="tk-exra">
          <span class="border">
            <img src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
            自营
          </span>
          <span class="border">条件退</span>
        </div>
      </div>
      <div class="tk-btn">
        <div class="tk-price">￥<em>298</em></div>
        <div class="tk-buy-btn">预定</div>
      </div>
    </div>
    <div class="tk-item border-top">
      <div class="tk-info">
        <h3 class="tk-title">【随买随用】《长恨歌》第一场中区</h3>
        <span class="tk-tips">
          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" alt="">
          可订明日
        </span>
        <div class="tk-exra">
          <span class="border">
            <img src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
            自营
          </span>
          <span class="border">条件退</span>
        </div>
      </div>
      <div class="tk-btn">
        <div class="tk-price">￥<em>298</em></div>
        <div class="tk-buy-btn">预定</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'detailTciketList'
}
</script>

<style lang="stylus" scoped>
  .tciketList >>> .border::before
    border-color: #a5e4ec
  .tciketList
    margin-bottom: .2rem
    padding-left: .2rem
    background-color: #fff
    .tk-title
      font-size: .32rem
      height: .88rem
      line-height: .88rem
      color: #333
    .tk-item
      display: flex
      padding: .2rem .2rem .24rem 0
      align-items: center
      .tk-info
        flex: 2.92
        .tk-title
          height: .52rem
          line-height: .52rem
          margin-right: .1rem
          padding-bottom: 0
          color: #616161
          font-size: .3rem
        .tk-tips
          display: inline-block
          height: .32rem
          color: #616161
          font-size: .24rem
          line-height: .32rem
          white-space: nowrap
          img
            width: .2rem
            vertical-align: 0
        .tk-exra
          span
            display: inline-block
            margin-top: .08rem
            padding: 0 .04rem
            height: .32rem
            color: #00afc7
            font-size: .2rem
            line-height: .32rem
            white-space: nowrap
            img
              width: .2rem
              vertical-align: 0
      .tk-btn
        flex: 1
        text-align: center
        padding-left: .5rem
        width: .2rem
        .tk-price
          color: #ff9800
          em
            font-size: .4rem
        .tk-buy-btn
          box-sizing: border-box
          padding: .16rem .2rem
          color: #fff
          background: linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
          font-size: .28rem
          border-radius: .08rem
</style>
