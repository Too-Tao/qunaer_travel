<template>
  <div class="wapper">
    <div class="like">
      <i class="iconfont" style="color: #FF6350">&#xe640;</i>
      猜你喜欢
    </div>
    <ul class="view-list">
      <li class="view" v-for="item in viewList" :key="item.id">
        <div class="view-msgImg" :style="{backgroundImage:'url(' + item.msgImg + ')'}">{{ item.msg }}</div>
        <div class="view-img">
          <img class="img" :src="item.img">
        </div>
        <div class="view-info">
          <div class="view-title">{{item.title}}</div>
          <div class="view-content">
            <span class="star">
              <Star :size="48" :star="item.star"/>
            </span>
            <span class="comment">{{item.comment}}</span>
          </div>
          <div class="price-address">
            <span class="price"><span style="color: #ff8300">￥<em style="fontSize: .4rem">{{item.price}}</em></span>起</span>
            <span class="address">红谷滩新区</span>
          </div>
        </div>
      </li>
    </ul>
    <div class="more border-top">查看所有产品</div>
  </div>
</template>

<script>
import Star from '../../../common/star/Star.vue'
export default {
  name: 'Recommed',
  components: {
    Star
  },
  data() {
    return {
      viewList: [
        {
          id: 1,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png',
          msg: '可定明日',
          img: 'http://img1.qunarzz.com/sight/p0/1610/88/88ec04f6d021724da3.water.jpg_200x200_d9307de0.jpg',
          title: '南昌融创电影乐园（原万达电影乐园）',
          star: '4',
          comment: '1372条评论',
          price: '170',
          address: '九龙湖新区'
        },
        {
          id: 2,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
          msg: '可订今日',
          img: 'http://img1.qunarzz.com/sight/p0/1610/83/83a873f755d64992a3.water.jpg_200x200_f7acbacd.jpg',
          title: '南昌融创主题乐园（原万达主题乐园）',
          star: '4.9',
          comment: '17199条评论',
          price: '170',
          address: '红谷滩新区'
        },
        {
          id: 3,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png',
          msg: '可定明日',
          img: 'http://img1.qunarzz.com/sight/p0/1610/16/165075d3fcbe7c8ba3.water.jpg_200x200_dacfbf65.jpg',
          title: '南昌融创海洋乐园（原万达海洋乐园）',
          star: '4.1',
          comment: '7403条评论',
          price: '90',
          address: '南昌'
        },
        {
          id: 4,
          msgImg: '',
          msg: '',
          img: 'http://img1.qunarzz.com/sight/p0/1701/c0/c0899de1bcef6f9a3.img.jpg_200x200_b5b00164.jpg',
          title: '南昌融创电影乐园（原万达电影乐园）',
          star: '3.9',
          comment: '193条评论',
          price: '86',
          address: '西湖区'
        },
        {
          id: 5,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png',
          msg: '可定明日',
          img: 'http://img1.qunarzz.com/sight/p0/1610/88/88ec04f6d021724da3.water.jpg_200x200_d9307de0.jpg',
          title: '南昌融创电影乐园（原万达电影乐园）',
          star: '3',
          comment: '1372条评论',
          price: '170',
          address: '九龙湖新区'
        },
        {
          id: 6,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png',
          msg: '可定明日',
          img: 'http://img1.qunarzz.com/sight/p0/1602/49/4917c5b8d400d5b890.img.jpg_200x200_4e55a084.jpg',
          title: '凤凰沟',
          star: '3.5',
          comment: '2075条评论',
          price: '24.5',
          address: '西湖区'
        },
        {
          id: 7,
          msgImg: 'https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png',
          msg: '可定明日',
          img: 'http://img1.qunarzz.com/sight/p0/1608/9c/9c744efe971f8966a3.water.jpg_200x200_3bfda054.jpg',
          title: '怪石岭生态公园（南昌长城）',
          star: '4.5',
          comment: '3966条评论',
          price: '39',
          address: '新建县'
        },
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wapper
    width 100%
    height auto
    .like
      padding .26rem
    .view-list
      margin-left .26rem
      .view
        position relative
        overflow hidden
        margin-bottom .4rem
        .view-msgImg
          position absolute
          left 0
          width 1.02rem
          height .38rem
          background-size 100%
          color #fff
          font-size .2rem
          line-height .38rem
          text-indent .04rem
        .view-img
          float left
          width 2rem
          height 2rem
          margin-right .22rem
          .img
            width 100%
            height 100%
        .view-info
          .view-title
            overflow hidden
            // width 100%
            white-space nowrap
            text-overflow ellipsis
            margin-top .26rem
            height 0.44rem
            color #212121
            font-size .32rem
            line-height .44rem
          .view-content
            margin-top 0.14rem
            height 0.34rem
            .star
              display inline-block
              position relative
              width 1.5rem
              height 0.28rem
              line-height .28rem
              font-size .28rem
              letter-spacing .2rem
            .comment
              margin-left .2rem
              color #616161
              font-size .24rem
              line-height .34rem
              vertical-align top
          .price-address
            position relative
            margin-top .22rem
            color #616161
            font-size .24rem
            line-height .4rem
            .address
              position absolute
              display inline-block
              width 1.16rem
              right .24rem
              bottom 0
              overflow hidden
              white-space nowrap
              text-overflow ellipsis
    .more
      width 100%
      padding .2rem 0
      height .2rem
      text-align center
      line-height .4rem
      color #00afc7
      font-size .28rem
      margin-bottom .2rem
</style>
