<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '01',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/2f5f3ea4698c9b7898db7562d89b91ed.jpg_750x200_bd3b4ce9.jpg'
        },
        {
          id: '02',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ad906cbe02849a504c4a4399741013a4.jpg_750x200_8ac64dcc.jpg'
        },
        {
          id: '03',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/9f73976e40c4ef845cabe0efc0269ebb.jpg_750x200_aab92b7a.jpg'
        },
        {
          id: '04',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/0a8f7c789d0e62966e2485d33bf7ebd3.jpg_750x200_b455610d.jpg'
        },
        {
          id: '05',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/31a560a7b8f9c26bc8121e141b25d5a6.png_750x200_2775ea25.png'
        },
        {
          id: '06',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/942d87cc1576c333c77dc1f86af145cd.jpg_750x200_d25bf3eb.jpg'
        },
        {
          id: '07',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ed5f4115226306e48e6fad106a038afe.jpg_750x200_64df48d6.jpg'
        },
        {
          id: '08',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/5e7826d84dc49b10abbf7d22a5677de6.png_750x200_cd22a451.png'
        },
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
      background #fff
  .wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom 26.6667%
    background #eeeeee
    .swiper-img
      width 100%
</style>
