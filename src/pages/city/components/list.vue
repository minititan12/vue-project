<template>
  <div class="cityList">
    <div class="cityList-item">
      <div class="item-title border-topbottom">当前城市</div>
      <div class="btn-list">
        <div class="btn">北京</div>
      </div>
    </div>
    <div class="cityList-item">
      <div class="item-title border-topbottom">热门城市</div>
      <div class="btn-list">
        <div class="btn">北京</div>
        <div class="btn">深圳</div>
        <div class="btn">广州</div>
        <div class="btn">重庆</div>
        <div class="btn">上海</div>
      </div>
    </div>
    <div class="cityList-item">
      <div class="item-title border-topbottom">A</div>
      <div class="item-list">
        <div class="item-text border-bottom">北京</div>
        <div class="item-text border-bottom">北京</div>
        <div class="item-text border-bottom">北京</div>
        <div class="item-text border-bottom">北京</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList'
}
</script>

<style lang="stylus" scoped>
  .cityList
    position: absolute
    top: 1.67rem
    left: 0
    right: 0
    bottom: 0
    .border-topbottom
      &:before
        border-color: #ccc
      &:after
        border-color: #ccc
    .item-title
      width: 100%
      height: .4rem
      background-color: #eee
      color: #666
      line-height: .4rem
      padding-left: .2rem
    .btn-list
      width: 100%
      box-sizing: border-box
      padding: .2rem .2rem 0 .2rem
      display: flex
      flex-direction: row
      flex-wrap: wrap
      .btn
        width: 30%
        height: .5rem
        line-height: .5rem
        text-align: center
        border: .02rem solid #ccc
        border-radius: .1rem
        margin-bottom: .2rem
        margin-right: .15rem
    .item-list
        width: 100%
        line-height: .65rem
        .item-text
          padding-left: .2rem
        .border-bottom
          &:before
            border-color: #ccc
</style>
