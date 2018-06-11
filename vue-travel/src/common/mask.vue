<template>
  <div @click="handleMaskClick" class="my-mask"></div>
</template>

<script>
export default {
  name: 'MyMask',
  methods: {
    handleMaskClick () {
      this.$emit('maskClick')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .my-mask
    position: absolute
    top: 0
    left: 0
    right: 0
    bottom: 0
    background-color: rgba(0, 0, 0, .5)
</style>
