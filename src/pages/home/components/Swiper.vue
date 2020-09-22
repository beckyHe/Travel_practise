<template>
<div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg"/>
    </swiper-slide>
    <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/sight/p0/1709/76/7691528bc7d7ad3ca3.img.png_800x800_9ef05ee7.png"/>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>

  </swiper>
</div>
</template>

<script>
export default {
    name: 'homeswiper',
    data() {
      return {
        swiperOptions: {
          pagination: '.swiper-pagination',
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    }
    
  }
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow hidden
        width 100%
        height 0
        padding-bottom 31.25%
        background #eee
        .swiper-img
            width: 100%

</style>