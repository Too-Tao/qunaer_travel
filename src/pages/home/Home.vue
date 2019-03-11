<template>
  <div>
    <home-header/>
    <home-swiper/>
    <home-icons/>
    <home-recommend-swiper/>
    <home-recommed/>
  </div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommendSwiper from './components/RecommedSwiper.vue'
import HomeRecommed from './components/Recommed.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommendSwiper,
    HomeRecommed
  }
}
</script>

<style lang="stylus" scoped>
</style>
