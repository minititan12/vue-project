<template>
  <div class="icons">
    <div class="icon" v-for="item of iconList" :key="item.id">
      <img class="icon-img" :src="item.iconImg"/>
      <span class="icon-title">{{item.title}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    iconList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/ellipsis.styl'
  .icons
    width: 100%
    height: 0
    padding-bottom: 45%
    display: flex
    flex-direction: row
    flex-wrap: wrap
    .icon
      display:flex
      flex-direction: column
      margin-top: .2rem
      text-align: center
      width: 25%
      .icon-img
        width: 50%
        padding-left: 25%
        padding-right: 25%
      .icon-title
        margin-top: .1rem
        ellipsis()
</style>
