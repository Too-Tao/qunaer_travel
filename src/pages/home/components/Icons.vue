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
export default {
  name: 'HomeIcons',
  data() {
    return {
      iconList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png',
          desc: '本地游玩'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
          desc: '自然风光'
        },
        {
          id: '004',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc: '一日游'
        },
        {
          id: '005',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
          desc: '游乐场'
        },
        {
          id: '006',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          desc: '泡温泉'
        },
        {
          id: '007',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc: '南昌必游'
        },
        {
          id: '008',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ec/0e1e0238e24ba02.png',
          desc: '婺源'
        },
        {
          id: '009',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
          desc: '融创乐园'
        },
        {
          id: '010',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
          desc: '全部玩乐'
        }
      ],
      swiperOption: {
        pagination: '.swiper-pagination',
        // loop: true
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
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
