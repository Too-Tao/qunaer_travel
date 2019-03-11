<template>
<div>
  <div class="title">热门推荐</div>
  <ul>
      <li class="item border-bottom">
        <div class="item-img-wrapper">
          <img class="item-img" src="http://img1.qunarzz.com/sight/p0/1610/88/88ec04f6d021724da3.water.jpg_200x200_d9307de0.jpg">
        </div>
        <div class="item-info">
          <p class="item-title">南昌融创电影乐园（原万达电影乐园）</p>
          <p class="item-desc"></p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
</div>
  
</template>

<script>
export default {
  name: 'HomeRecommend'
}
</script>

<style lang="stylus" scoped>
  .title
    line-height .8rem
    margin-top .2rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    // background green 
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
</style>
