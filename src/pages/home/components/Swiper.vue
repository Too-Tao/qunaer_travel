<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item in swiperlist" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  props: ['swiperlist'],
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
    };
  }
};
</script>

<style lang="stylus" scoped>
  // 更改swiper小圆点的背景色
  .wrapper >>> .swiper-pagination-bullet-active
      background #fff
  .wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom 26.6667%
    background #eeeeee
    .swiper-img
      width 100%
</style>
