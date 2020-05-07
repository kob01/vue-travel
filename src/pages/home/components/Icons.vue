<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.iconUrl" />
          </div>
          <p class="icon-desc">{{ item.iconName }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data() {
    return {
      iconList: [
        {
          id: '0001',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          iconName: '东方盐湖城',
        },
        {
          id: '0002',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          iconName: '景点门票',
        },
        {
          id: '0003',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
          iconName: '亲子游',
        },
        {
          id: '0004',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
          iconName: '踏青赏花',
        },
        {
          id: '0005',
          iconUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
          iconName: '自然风光',
        },
        {
          id: '0006',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          iconName: '常州必游',
        },
        {
          id: '0007',
          iconUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b71c1387a921ccf9c6edc7e8def3da90.png',
          iconName: '淹城动物园',
        },
        {
          id: '0008',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          iconName: '中华恐龙园',
        },
        {
          id: '0009',
          iconUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          iconName: '溧阳天目湖',
        },
      ],
    }
  },
  computed: {
    pages() {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    },
  },
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
  height 0
  padding-bottom 50%
.icon
  position relative
  float left
  width 25%
  height 0
  padding-bottom 25%
  .icon-img
    position absolute
    top 0.2rem
    left 0.3rem
    right 0
    bottom .44rem
    box-sizing border-box
    padding .1rem
    width 1.3rem
    height 1.3rem
    .icon-img-content
      display block
      margin 0 auto
      height 100%
  .icon-desc
    position absolute
    bottom 0
    left 0
    right 0
    height .44rem
    line-height .44rem
    color $darkTextColor
    text-align center
    overflow hidden
    white-space nowrap
    text-overflow ellipsis
    ellipsis()
</style>
