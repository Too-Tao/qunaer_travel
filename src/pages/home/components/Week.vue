<template>
  <div class="list border-top">
    <div class="week">周末去哪儿</div>
    <ul class="week-ul">
      <li class="week-li" v-for="item in weeklist" :key="item.id">
        <div class="list-img" :style="{backgroundImage:'url(' + item.img + ')'}"></div>
        <div class="listMsg">
          <div class="list-title">{{ item.title }}</div>
          <div class="list-content">{{ item.content }}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Week',
  props: ['weeklist'],
}
</script>

<style lang="stylus" scoped>
  .list
    width 100%
    height auto
    .week
      padding .26rem
      background #eeeeee
    .week-ul
      .week-li
        .list-img
          overflow hidden
          width 100%
          height 0
          padding-bottom 40%
          // background-image url("http://img1.qunarzz.com/sight/source/1505/bd/688c12889af7ad.jpg_r_640x214_cc490c32.jpg")
          background-size 100% 100%
        .listMsg
          .list-title
            width 100%
            height auto
            padding .26rem 0 0 .28rem
            text-overflow ellipsis
            white-space nowrap
            color #212121
          .list-content
            width 100%
            height auto
            padding .26rem
            overflow hidden
            color #616161
            font-size .24rem
            line-height .42rem
            white-space nowrap
            text-overflow ellipsis
</style>
