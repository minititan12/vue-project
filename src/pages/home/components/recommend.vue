<template>
  <div class="recommend-wraper">
    <div class="recommend-title">热销推荐</div>
    <div class="recommend-list" v-for="item of recommendList" :key="item.id">
      <div class="recommend-item">
        <img class="recommend-img" :src="item.recommendImg">
        <div class="recommend-info">
          <span class="info-title">{{item.title}}</span>
          <span class="info-content">{{item.content}}</span>
          <span class="info-btn">查看详情</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/ellipsis.styl'
  .recommend-wraper
    width : 100%
    .recommend-title
      width: 100%
      height: .8rem
      background-color: #eee
      line-height: .8rem
      text-indent: .2rem
      font-weight: bold
    .recommend-list
      width: 100%
      display: flex
      flex-direction: column
      .recommend-item
        width: 100%
        padding: .1rem
        display: flex
        flex-direction: row
        align-items: center
        .recommend-img
          width: 25vw
          height: 20vw
        .recommend-info
          display: flex
          flex-direction: column
          flex-grow: 1
          margin-left: .2rem
          .info-title
            font-size: .3rem
            font-weight: bold
            ellipsis()
          .info-content
            color: #ccc
            line-height: .5rem
            ellipsis()
          .info-btn
            display: block
            width: 1.3rem
            background-color: orange
            padding: .1rem
            text-align: center
            border-radius: .05rem
</style>
