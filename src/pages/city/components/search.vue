<template>
  <div class="searchWraper">
    <input type="text" class="searchInput" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  .searchWraper
    width: 100%
    height: .6rem
    padding: .1rem
    background-color: #00bcd4
    .searchInput
      box-sizing: border-box
      width: calc(100% - .2rem)
      font-size: .3rem
      line-height: .6rem
      text-align: center
      border-radius: .1rem
      padding: 0 .1rem
</style>
