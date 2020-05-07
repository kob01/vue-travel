<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data() {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true,
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'https://n1-q.mafengwo.net/s16/M00/A3/0B/CoUBUl6q5ZqAbgiwAA1iAsQ5FyI188.jpg?imageMogr2%2Fthumbnail%2F%21450x270r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21450x270%2Fquality%2F90',
        },
        {
          id: '0002',
          imgUrl:
            'https://b1-q.mafengwo.net/s16/M00/93/B8/CoUBUl6oE3uAVp6dABBX482gwC0905.jpg?imageMogr2%2Fthumbnail%2F%21450x270r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21450x270%2Fquality%2F90',
        },
        {
          id: '0003',
          imgUrl:
            'https://p1-q.mafengwo.net/s16/M00/D0/FE/CoUBUl6uv8-AGt5VAAezaF2eYa464.jpeg?imageMogr2%2Fthumbnail%2F%21450x270r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21450x270%2Fquality%2F90',
        },
        {
          id: '0004',
          imgUrl:
            'https://n1-q.mafengwo.net/s12/M00/E3/15/wKgED1xGsy2AJ8gVAAU_Ajm-ud046.jpeg?imageMogr2%2Fthumbnail%2F%21450x270r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21450x270%2Fquality%2F90',
        },
      ],
    }
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
