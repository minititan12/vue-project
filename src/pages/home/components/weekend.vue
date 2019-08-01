<template>
  <div class="weekend-wraper">
    <div class="weekend-title">周末去哪儿</div>
    <div class="weekend-list" v-for="item of weekendList" :key="item.id">
      <div class="weekend-item">
        <img class="weekend-img" :src="item.recommendImg">
        <div class="weekend-info">
          <span class="info-title">{{item.title}}</span>
          <span class="info-content">{{item.content}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/ellipsis.styl'
  .weekend-wraper
    width : 100%
    .weekend-title
      width: 100%
      height: .8rem
      background-color: #eee
      line-height: .8rem
      text-indent: .2rem
      font-weight: bold
    .weekend-list
      width: 100%
      display: flex
      flex-direction: column
      .weekend-item
        width: 100%
        padding: .1rem
        display: flex
        flex-direction: column
        .weekend-img
          width: calc(100% - .2rem)
        .weekend-info
          display: flex
          flex-direction: column
          .info-title
            font-size: .3rem
            line-height: .5rem
            font-weight: bold
            ellipsis()
          .info-content
            color: #ccc
            ellipsis()
</style>
