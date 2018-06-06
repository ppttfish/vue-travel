<template>
  <div class="home-recommend">
    <div class="recommend-title">推荐攻略</div>
     <a v-for="item of list" :key="item.id" class="recommend-block border-bottom">
      <div class="title">{{ item.title }}</div>
      <div class="main-body">
        <img :src="item.imgUrl" class="recommend-img" alt="">
        <div class="summary">{{ item.summary }}</div>
        <div class="extra">
          270315浏览
          <div class="btn">问答</div>
        </div>
      </div>
    </a>
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
    text-align: center
    .recommend-title
      color: #999
      height: .6rem
      line-height: .6rem
      background-color: #f8f8f8
    .recommend-block
      display: block
      box-sizing: border-box
      min-height: 3rem
      padding: .25rem
      color: black
      .title
        text-align: left
        font-size: .4rem
        font-weight: 300
        font-family: 'PingFangSC-Light',Arial,Helvetica,sans-serif,"Hiragino Sans GB";
      .main-body
        overflow: hidden
        position: relative
        .recommend-img
          width: 2.59rem
          height: 1.8rem
          margin-top: .2rem
          margin-right: .18rem
          float: left
        .summary
          ellipsis(3)
          text-align: left
          padding-top: .3rem
          color: #999
          line-height: .36rem
          overflow: hidden
        .extra
          position: absolute
          box-sizing: border-box
          padding-left: 2.8rem
          text-align: left
          width: 100%
          left: 0
          bottom: 0
          line-height: .4rem;
          color: #999
          font-size: .25rem
          .btn
            position: absolute
            bottom: 0
            right: 0
            border-color: #30d2bf;
            color: #30d2bf;
            border: 1px solid;
            border-radius: 3px;
            font-size: .1rem;
            padding: 0 0.15rem;
</style>
