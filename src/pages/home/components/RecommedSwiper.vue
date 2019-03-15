<template>
  <div class="wrapper">
    <div class="wrapper-content">
      <span class="wrapper-title">本周热门榜单</span>
      <span class="full-list">全部榜单</span>
      <div class="swiper">
        <ul class="list">
          <li class="list-item" v-for="item in viewlist " :key="item.id">
            <a href="#">
              <div class="item-num">
                <img class="item-num-img" :src="item.rankImg" v-show="item.rank < 4">
              </div>
              <div class="item-img">
                <img class="item-img-img" :src="item.img">
              </div>
              <div class="item-title">{{item.title}}</div>
              <div class="item-price"><span style="color: #ff8300">￥<em style="fontSize: .28rem">{{item.price}}</em></span>起</div>
            </a>
          </li>
        </ul>
      </div>
    </div>
    
    
  </div>
</template>

<script>
export default {
  name: 'RecommedSwiper',
  props: [ 'viewlist' ]
}
</script>

<style lang="stylus" scoped>
  .wrapper
    position relative
    width 100%
    height 4.1rem
    margin-top 1rem
    background #eeeeee
    .wrapper-content
      position absolute
      width 100%
      height 3.8rem
      top .16rem
      // margin-top .3rem
      background #ffffff
      .wrapper-title
        display inline-block
        float left
        padding .26rem
      .full-list
        float right
        padding .24rem
      .swiper
        position inherit
        width 100%
        top .8rem
        height 3rem
        // background #008000
        .list
          overflow-x auto
          white-space nowrap
          width auto
          .list-item
            position relative
            width 2rem
            height 3rem
            margin-left .2rem
            display inline-block
            // background green
            .item-num
              position absolute
              top 0
              left 0;
              z-index: 1
              overflow: hidden
              width: .84rem
              height: .4rem
              // background red
              .item-num-img
                width 100%
                height 100%
                border-radius .1rem
                overflow hidden
            .item-img
              width 2rem
              height 2rem
              background #eeeeee
              .item-img-img
                width 100%
                height 100%
            .item-title
              color #212121
              font-size: .24rem
              line-height .32rem
              text-align center
              overflow hidden
              width 100%
              white-space nowrap
              text-overflow ellipsis
              margin-top .1rem
            .item-price
              color #616161
              font-size .24rem
              line-height .36rem
              text-align center
              margin-top .1rem
</style>
