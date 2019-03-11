<template>
  <div class="list border-top">
    <div class="week">周末去哪儿</div>
    <ul class="week-ul">
      <li class="week-li" v-for="item in weekList" :key="item.id">
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
  data() {
    return {
      weekList: [
        {
          id: 1,
          img: 'http://img1.qunarzz.com/sight/source/1505/bd/688c12889af7ad.jpg_r_640x214_cc490c32.jpg',
          title: 'happy乐园',
          content: '在这里玩转乐园，疯玩起来，无忧无虑一整天！'
        },
        {
          id: 2,
          img: 'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          content: '看山看水，看看历史对南昌的浸润'
        },
        {
          id: 3,
          img: 'http://img1.qunarzz.com/sight/source/1505/df/9bcc134d126bc4.jpg_r_640x214_58a1f389.jpg',
          title: '陶醉青山绿水',
          content: '一年四季景色秀丽，层峦叠嶂，岩石高高耸立，白雾弥漫，犹如人间仙境'
        },
        {
          id: 4,
          img: 'http://img1.qunarzz.com/sight/source/1811/24/30f714149293b6.jpg_r_640x214_bfa37f12.jpg',
          title: '狮子峰等你',
          content: '有黄山之险，悬崖峭壁，这里有满山的翠竹、青藤，堪称人间仙境世外桃源'
        },
        {
          id: 5,
          img: 'http://img1.qunarzz.com/sight/source/1505/d7/0833d5e316d76f.jpg_r_640x214_258e1eb8.jpg',
          title: '当地特色',
          content: '独特的自然景色，历史遗留景观，是南昌的特色。'
        }
      ]
    }
  }
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
