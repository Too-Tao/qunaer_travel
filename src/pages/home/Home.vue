<template>
  <div>
    <home-header/>
    <home-swiper/>
    <home-icons/>
    <home-recommend-swiper/>
  </div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommendSwiper from './components/RecommedSwiper.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommendSwiper
  }
}
</script>

<style>

</style>
