<template>
  <div>
    <home-header/>
    <home-swiper/>
    <home-icons/>
    <home-recommend-swiper/>
    <home-recommed/>
    <home-week/>
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
  }
}
</script>

<style lang="stylus" scoped>
</style>
