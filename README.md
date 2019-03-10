# qunaer_travel
Vue实现去哪儿部分功能

# 那些坑们
## vue-awesome-swiper swiper没有高度的情况下会报错
## vue-awesome-swiper 用 ^2.6.7版的 高版本有问题

# 对于图片宽高比解决办法
## 第一种
```
  width 100%
  height 0
  overflow hidden
  padding-bottom 31.25%
```
## 第二种(有兼容性问题)
```
width 100%
height 34.25vw
```