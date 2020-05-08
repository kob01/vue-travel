<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array,
  },
  data() {
    return {
      swiperOptions: {
        notNextTick: true,
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 5000,
        speed: 800,
      },
    }
  },
  computed: {
    showSwiper() {
      return this.list.length
    },
  },
}
</script>

<style lang="stylus" scoped>
.wrapper>>>.swiper-pagination-bullet-active
  background-color #fff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 60%
  .swiper-img
  // height 4.5rem
    width 100%
</style>
