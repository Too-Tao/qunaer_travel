<template>
  <div>
    <home-header/>
    <home-swiper :swiperlist="list.swiperList"/>
    <home-icons/>
    <home-recommend-swiper :viewlist="list.viewList"/>
    <home-recommed/>
    <home-week :weeklist="list.weekList"/>
    <home-copyright/>
  </div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommendSwiper from './components/RecommedSwiper.vue'
import HomeRecommed from './components/Recommed.vue'
import HomeWeek from './components/Week.vue'
import HomeCopyright from './components/Copyright.vue'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommendSwiper,
    HomeRecommed,
    HomeWeek,
    HomeCopyright
  },
  data() {
    return {
        list: {
        }
    }
  },
  created() {
    //使用mock的方式获取数据，然后将数据传入子组件
    axios
      .get('https://www.easy-mock.com/mock/5c8b17ff7829617514a4dca9/data')
      .then(res => {     
        this.list = res.data
      })
  },
}
</script>

<style lang="stylus" scoped>
</style>
