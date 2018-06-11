<template>
  <div id="app">
    <keep-alive exclude="Details">
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="stylus" scoped>
  #app
     background-color: #fff
  h1,h2,h3,h4,h5,h6
    font-family: tahoma,arial,"Hiragino Sans GB","\5FAE\8F6F\96C5\9ED1",simsun,sans-serif;
</style>
