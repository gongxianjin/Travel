<!--suppress ALL -->
<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" alt="">
            </swiper-slide>
            <!-- Optional controls -->
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
        pagination:'.swiper-pagination',
        loop:true
      },
      swiperList: [{
        id:'0001',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg'
      },{
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1808/7e/19b06067afac3402.jpg_750x200_f613313a.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
     background: #FFF
    .wrapper
     overflow:hidden
     width:100%
     height:0
     padding-bottom:31.25%
     background:#eee
    .swiper-img
        width: 100%
</style>
