<template>
  <div class="star" :class="starType">
    <span :key="index" v-for="(itemClass,index) in itemClasses" :class="itemClass" class="star-item"></span>
  </div>
</template>

<script>
const LENGTH = 5
const CLS_ON = 'on'
const CLS_HALF = 'half'
const CLS_OFF = 'off'
export default {
  name: 'Star',
  props: {
    size: {
      type: Number
    },
    star: {
      type: Number
    }
  },
  computed: {
    starType: function () {
      return 'star-' + this.size
    },
    itemClasses: function () {
      let result = []
      let star = Math.floor(this.star * 2) / 2
      let hasDecimal = star % 1 !==0
      let integer = Math.floor(star)
      for (let i = 0; i < integer; i ++) {
        result.push(CLS_ON)
      }
      if (hasDecimal) {
        result.push(CLS_HALF)
      }
      while (result.length < LENGTH) {
        result.push(CLS_OFF)
      }
      return result
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/mixins.styl'
  .star
    font-size 0
    .star-item
      display inline-block
      background-repeat no-repeat
    &.star-48
      .star-item
        width .2rem
        height .2rem
        margin-right .1rem
        background-size .22rem .22rem
        &:last-child
          margin-right: 0
        &.on
          bg-image('star48_on')
        &.half
          bg-image('star48_half')
        &.off
          bg-image('star48_off')
    &.star-36
      .star-item
        width .2rem
        height .2rem
        margin-right .1rem
        background-size .22rem .22rem
        &:last-child
          margin-right: 0
        &.on
          bg-image('star36_on')
        &.half
          bg-image('star36_half')
        &.off
          bg-image('star36_off')
    &.star-24
      .star-item
        width .2rem
        height .2rem
        margin-right .1rem
        background-size .22rem .22rem
        &:last-child
          margin-right: 0
        &.on
          bg-image('star24_on')
        &.half
          bg-image('star24_half')
        &.off
          bg-image('star24_off')
</style>
