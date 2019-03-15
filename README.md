# 项目描述
> 使用Vue实现去哪儿网webapp版功能
# 项目展示
![img](https://github.com/Too-Tao/qunaer_travel/blob/master/qunar.gif)
# 技术栈
Vue ES6 (loading....)
# 实现的功能
## 首页
* 图片轮播
* swiper滑块
* 数据呈现
# 遇上的Bug以及解决办法
## vue-awesome-swiper的坑
    vue-awesome-swiper swiper没有高度的情况下会报错
    vue-awesome-swiper 用 ^2.6.7版的 高版本有问题
    swiper需要滚动跳转时 在 swiperOption 下添加 ```loop: true```
    swiperOption中绑定class注意去加'.'
    
    pagination: '.swiper-pagination'
    

## 对于图片宽高比解决办法
### 第一种
```
  width 100%
  height 0
  overflow hidden
  padding-bottom 31.25%
```
### 第二种(有兼容性问题)
```
width 100%
height 34.25vw
```

## 值得注意的细节
    img标签 用 v-bind指令监听src地址的改变 :src
    swiper需要滚动跳转时 在 swiperOption 下添加 loop: true
    ~@ 表示src