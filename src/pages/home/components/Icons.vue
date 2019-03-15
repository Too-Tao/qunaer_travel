<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div 
          class="icon"
          v-for="item in page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{ item.desc }}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    <div class="icon-block border-top">
      <span class="block-left  border-right">
        <i class="iconfont iconfont-size1">&#xe87e;</i>
        定位失败</span>
      <span class="block-right ">
        <i class="iconfont iconfont-size2">&#xe888;</i>
        必游榜单</span>
    </div>
  </div>
  
</template>

<script>
import axios from 'axios'
export default {
  name: 'HomeIcons',
  data() {
    return {
      iconList: [],
      swiperOption: {
        pagination: '.swiper-pagination',
        // loop: true
      }
    }
  },
  created() {
    axios
      .get('https://www.easy-mock.com/mock/5c8b17ff7829617514a4dca9/data')
      .then( res => {
        this.iconList = res.data.iconList
      })
  },
  computed: {
    //计算pages 总共有多少跳数据
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        //每页设置8条数据
        const page = Math.floor(index / 8)
        if ( !pages[page] ) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
@import '~@/assets/styles/mixins.styl'
  .icons >>> .swiper-container
  .icons
    margin-top .1rem
    height 0
    padding-bottom 50%
    .icon
      position relative
      overflow hidden
      width 25%
      float left
      padding-bottom 23%
      // background red
      .icon-img
        position absolute
        top 0
        right 0
        left 0
        bottom .44rem
        // background blue
        box-sizing border-box
        padding .1rem
        .icon-img-content
          display block
          margin 0 auto 
          // width 100%
          height 100%
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height 0.44rem
        line-height 0.44rem
        text-align center
        color $darkTextColor
        ellipsis()
  .icon-block
    display flex
    width 100%
    height 0.98rem
    font-size 0
    // padding-bottom 10%
    // background green
    .block-left
      float left
      width 50%
      line-height .98rem
      text-align center
      font-size .28rem
      .iconfont-size1
        font-size .26rem
    .block-right
      flex 1
      text-align center
      line-height .98rem
      font-size .28rem
      .iconfont-size2
        font-size .32rem
</style>
