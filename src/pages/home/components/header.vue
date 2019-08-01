<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe658;</span></div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      <span class="text">输入城市/景点/游玩主题</span>
    </div>
    <router-link to="/city">
      <div class="header-right">
          <span class="text">城市</span>
          <span class="iconfont">&#xe65c;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    flex-direction: row
    align-items: center
    height: .86rem
    background: #00bcd4
    color: #fff
    .header-left
      width: .64rem
      margin-left: .2rem
      .iconfont
        font-size: .5rem
        line-height: .86rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-left: .1rem
      padding-left: .4rem
      background: #ffffff
      border-radius: .1rem
      color: #ccc
      .iconfont
        vertical-align: middle
      .text
        vertical-align: middle
    .header-right
      width: 1.24rem
      height: 100%
      line-height: .86rem
      text-align: center
      color: #fff
      .iconfont
        font-size: .5rem
        vertical-align: middle
        margin-left: -.2rem
      .text
        vertical-align: middle
</style>
