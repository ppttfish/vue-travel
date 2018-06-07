<template>
  <div class="city-list">
    <h2>热门城市</h2>
    <ul class="mp-list">
      <li v-for="hotCity of cityData.hotCities" :key="hotCity.id">
        <a>{{ hotCity.name }}</a>
      </li>
    </ul>
    <h2>字母排序</h2>
    <ul class="mp-list alphabet-list">
      <li v-for="letter of alphabet" :key="letter">
        <a :href="'#domestic-' + letter">{{ letter }}</a>
      </li>
    </ul>
    <div v-for="(cities, key) of cityData.cities" :key="key">
      <a :id="'domestic-' + key"></a>
      <h2 >{{ key }}</h2>
      <ul class="mp-list">
        <li v-for="city of cities" :key="city.id">
          <a>{{ city.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList',
  props: {
    cityData: Object
  },
  data () {
    return {
      alphabet: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
    }
  }
}
</script>

<style lang="stylus" scoped>
  .city-list
    overflow hidden
    h2
      font-size: .24rem
      margin: .24rem .3rem
    .mp-list
      background-color: #fff
      position: relative
      overflow hidden
      &::before
        content: ''
        position: absolute
        width: 25%
        left: 25%
        height: 100%
        border-left: .02rem solid #ddd
        border-right: .02rem solid #ddd
      &::after
        content: ''
        position: absolute
        width: 25%
        left: 50%
        height: 100%
        border-right: .02rem solid #ddd
      &.mp-list-tr3
        li
          width: 33.3%
        &::before
          width: 33.3%
          left: 33.3%
        &::after
           border: 0
      &.alphabet-list
        padding: .3rem 0;
        li
          border: 0
          width: 16.66%
        &::before
        &::after
          border: 0
      li
        display: inline-block
        position: relative
        width: 25%
        float: left
        height: .9rem;
        line-height: .9rem;
        font-size: .28rem;
        text-align: center
        border-bottom: .02rem solid #ddd;
        margin-bottom: -1px;
        z-index: 1
        a
          color: black
</style>
