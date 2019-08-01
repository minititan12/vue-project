<template>
  <div class="city-header">
    <router-link to="/">
      <span class="iconfont">&#xe658;</span>
    </router-link>
    <span class="header-title">城市选择</span>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  .city-header
    position: relative
    width: 100%
    height: .86rem
    background-color: #00bcd4
    text-align: center
    line-height: .86rem
    font-weight: bold
    color: #fff
    .iconfont
      position: absolute
      top: 0;
      left: .1rem
      font-size: .5rem
      color: #fff
</style>
