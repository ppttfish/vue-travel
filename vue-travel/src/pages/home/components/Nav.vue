<template>
  <ul class="nav-ul">
    <li class="nav-li" v-for="item of list" :key="item.id">
      <a href="" :class="item.class">
        <i></i>
        <p>{{ item.name }}</p>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'NavList',
  data () {
    return {
      list: [
        {
          id: '0001',
          name: '找攻略',
          class: 'i1'
        },
        {
          id: '0002',
          name: '看游记',
          class: 'i2'
        },
        {
          id: '0003',
          name: '问达人',
          class: 'i3'
        },
        {
          id: '0004',
          name: '结伴',
          class: 'i4'
        },
        {
          id: '0005',
          name: '酒店',
          class: 'i5'
        },
        {
          id: '0006',
          name: '旅行商城',
          class: 'i6'
        },
        {
          id: '0007',
          name: '机票',
          class: 'i7'
        },
        {
          id: '0008',
          name: '当地玩乐',
          class: 'i8'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scope>
  .nav-ul
    overflow: hidden
    height: 0
    padding-bottom: 40%
    margin: .2rem 0
    .nav-li
      box-sizing: border-box
      float: left
      width: 25%
      height: 0
      padding-bottom: 20%
      text-align: center
      .i1
        color: #ff9d00;
        i
          background-position: .01rem 0
      .i2
        color: #feca2b;
        i
          background-position: 0 -.98rem
      .i3
        color: #42d6ba;
        i
          background-position: -1.96rem -.98rem
      .i4
        color: #f94a87;
        i
          background-position: -.98rem -.98rem
      .i5
        color: #32a2f1;
        i
          background-position-x: -.98rem
      .i6
        color: #fd4e4e;
        i
          background-position-x: -1.96rem
      .i7
        color: #acce0e;
        i
          background-position-x: -2.94rem
      .i8
        color: #b160df;
        i
          background-position: -2.94rem -.98rem
      i
        display: inline-block
        width: .99rem
        height: .99rem
        background: blue
        background: url(/static/img/i_nav3.png) no-repeat
        background-size: 4rem
</style>
