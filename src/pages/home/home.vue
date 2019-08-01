<template>
  <div>
    <home-header></home-header>
    <HomeSwiper :swiperList="swiperList"></HomeSwiper>
    <HomeIcons :iconList="iconList"></HomeIcons>
    <HomeRecommend :recommendList="recommendList"></HomeRecommend>
    <HomeWeekend :weekendList="weekendList"></HomeWeekend>
  </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/recommend'
import HomeWeekend from './components/weekend'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      iconList: [],
      recommendList: [],
      swiperList: [],
      weekendList: []
    }
  },
  mounted: function () {
    this.getHomeInfo()
  },
  methods: {
    getHomeInfo () {
      axios.get('https://easy-mock.com/mock/5d428ef64a056827b4884db6/api/data/api/data/homeInfo')
        .then((res) => {
          this.getHomeInfoSucc(res)
        })
        .catch((err) => {
          console.log('get homeInfo err' + err)
        })
    },
    getHomeInfoSucc (res) {
      let data = res.data
      if (data.success && data.homeInfo) {
        this.iconList = data.homeInfo.iconList
        this.recommendList = data.homeInfo.recommendList
        this.swiperList = data.homeInfo.swiperList
        this.weekendList = data.homeInfo.weekendList
      }
    }
  }
}
</script>

<style>
</style>
