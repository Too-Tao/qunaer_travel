<template>
  <div class="wrapper">
    <div class="wrapper-content">
      <span class="wrapper-title">本周热门榜单</span>
      <span class="full-list">全部榜单</span>
      <div class="swiper">
        <ul class="list">
          <li class="list-item" v-for="item in viewList " :key="item.id">
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
  data() {
    return {
      viewList: [
        {
          id: 1,
          rank: 1,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1610/88/88ec04f6d021724da3.water.jpg_250x250_8534ae09.jpg',
          title: '南昌融创电影乐园（原万达电影乐园）',
          price: '170'
        },
        {
          id: 2,
          rank: 2,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
          img: 'http://img1.qunarzz.com/sight/p0/1610/16/165075d3fcbe7c8ba3.water.jpg_250x250_5381d250.jpg',
          title: '南昌融创海洋乐园（原万达海洋乐园）',
          price: '90'
        },
        {
          id: 3,
          rank: 3,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
          img: 'http://img1.qunarzz.com/sight/p0/1609/94/945ab5b76758703a3.water.jpg_250x250_ff0fb518.jpg',
          title: '滕王阁',
          price: '170'
        },
        {
          id: 4,
          rank: 4,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1411/25/0ef2f8ab5cca36253ef726a113c8e6f5.water.jpg_250x250_d78a3930.jpg',
          title: '梅岭景区',
          price: '170'
        },
        {
          id: 5,
          rank: 5,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/201301/08/1d7adb4e163cc8e493835fbb.png_250x250_940ffcd2.png',
          title: '南昌之星游乐园',
          price: '170'
        },
        {
          id: 6,
          rank: 6,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1610/83/83a873f755d64992a3.water.jpg_250x250_64f48168.jpg',
          title: '南昌融创主题乐园（原万达主题乐园）',
          price: '170'
        },
        {
          id: 7,
          rank: 7,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
          img: 'http://img1.qunarzz.com/sight/p0/1609/94/945ab5b76758703a3.water.jpg_250x250_ff0fb518.jpg',
          title: '滕王阁',
          price: '170'
        },
        {
          id: 8,
          rank: 8,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1701/c0/c0899de1bcef6f9a3.img.jpg_250x250_59e860cb.jpg',
          title: '南昌新中原大剧院',
          price: '86'
        },
        {
          id: 9,
          rank: 9,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/201310/08/8a668cb269731796c8d65eac.png_250x250_416ab61e.png',
          title: '南昌琴岛之夜',
          price: '85'
        },
        {
          id: 10,
          rank: 10,
          rankImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1410/21/67f72f6b54ede94fae27e32d6ba92ae5.jpg_250x250_423208b7.jpg',
          title: '南昌天沐温泉',
          price: '49'
        },

      ]
    }
  }
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
