<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/2003/44/444588ea3ce27500a3.water.jpg_200x200_19f89d08.jpg',
          title: '东方盐湖城·道天下',
          desc: '华东地区最奇幻，最浪漫的道天下',
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1505/60/60e4722f8914f5c1.water.jpg_250x250_ae17c50f.jpg',
          title: '天目湖南山竹海景区',
          desc: '华东地区最奇幻，最浪漫的道天下',
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1807/c9/c9b31bce950940bda3.img.jpg_250x250_7dc6e7c3.jpg',
          title: '中华恐龙园',
          desc: '华东地区最奇幻，最浪漫的道天下',
        },
        {
          id: '0004',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1703/64/647673153b3d42ca3.img.jpg_200x200_d775cfe2.jpg',
          title: '江南环球港世界港口小镇',
          desc: '华东地区最奇幻，最浪漫的道天下',
        },
      ],
    }
  },
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top .2rem
  line-height .8rem
  background-color #eee
  text-indent .2rem
.item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0 .2rem
      border-radius .06rem
      color #fff
</style>
