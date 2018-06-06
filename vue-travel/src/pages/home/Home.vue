<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <nav-list></nav-list>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import NavList from './components/Nav'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    NavList
  }
}
</script>

<style>

</style>
