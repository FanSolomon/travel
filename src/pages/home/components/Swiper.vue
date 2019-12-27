<template>
    <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 4000
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/37c4edf7c033ada7b61a1f9d0acffd08.jpg_750x200_3223c943.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/4400f4a848b1f5920c64b801deba4692.jpg_750x200_c9a739ba.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/8c54576e74c6d4ea0062c9a664035262.jpg_750x200_9a39efd3.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.67%
    background: #eee
    .swiper-img
        width: 100%
</style>
