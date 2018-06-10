<template>
  <div class="item-baseinfo">
    <div class="flex-item flex-card">
      <div class="left-card border-right">
        <div>
          <span class="item-score">4.9</span>
          <span class="score-card-text">分</span>
          <span class="score-card-text">很棒</span>
        </div>
        <div>
          <span class="card-text">8687条评论</span>
          <span class="card-text">4条攻略</span>
          <span class="iconfont card-right-arrow">&#xe601;</span>
        </div>
      </div>
      <div class="right-card">
        <div>
          <span class="card-title right-card-text">景点简介</span>
        </div>
        <div>
          <span class="card-text right-card-text">开放时间、贴士</span>
        </div>
      </div>
    </div>
    <div class="item-address border-top">
      <span class="iconfont item-address-icon">&#xe679;</span>
      <p>陕西省西安市临潼区华清路38号华清池</p>
      <span class="iconfont right-arrow">&#xe601;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBaseInfo'
}
</script>

<style lang="stylus" scoped>
  .item-baseinfo
    position: relative
    top: -.1rem
    padding: .1rem .2rem 0 .2rem
    margin-bottom: .1rem
    background: #fff
    border-radius: .1rem .1rem 0 0
    .flex-card
      display: flex
      height: 40px
      padding-top: .1rem;
      padding-bottom: .2rem;
      .card-text
        font-size: .24rem
        color: #9e9e9e
        line-height: .32rem
        margin-right: .16rem
      .right-card-text
        padding-left: .3rem
      .left-card
        position: relative
        flex: 1
        .item-score
          font-size: .44rem
          color: #ff8300
          line-height: .44rem
        .score-card-text
          font-size: .28rem
          color: #ff8300
          line-height: .48rem
        .card-right-arrow
          position: absolute
          top: .2rem
          right: .1rem
          color: #9e9e9e
          font-size: .42rem
      .right-card
        position: relative
        flex: 1
        .card-title
          font-size: .28rem
          color: #212121
          line-height: .48rem
    .item-address
      position: relative
      padding: .2rem 0
      line-height: .36rem
      color: #212121
      .item-address-icon
        position: absolute
        left: 0
        margin-right: .2rem
        color: #9e9e9e
        font-size: .36rem
      p
        padding-right: .56rem
        position: relative
        padding-left: .56rem
      .right-arrow
        position: absolute
        top: .22rem
        right: 0
        color: #9e9e9e
        font-size: .45rem
</style>
