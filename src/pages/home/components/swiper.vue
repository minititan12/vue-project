<template>
  <div class="wraper">
    <swiper :options="swiperOption">
      <!-- slides -->
        <swiper-slide v-if="swiperList" v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgurl"/>
        </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      }
    }
  },
  props: {
    swiperList: Array
  }
}
</script>

<style lang='stylus' scoped>
  .wraper >>> .swiper-pagination-bullet-active
    background: #fff
  .wraper
    width: 100%
    height: 0
    padding-bottom: 30.5%
    background-color: #eee
    .swiper-img
      width: 100%
</style>
