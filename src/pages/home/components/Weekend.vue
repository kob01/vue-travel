<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <div class="item-img-wraper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/fd61f19f3f1cc1.jpg_r_640x214_6ebc0c51.jpg',
          title: '觅龙城的故事',
          desc: '两千多年历史的常州，道不尽悠悠历史',
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/3b/90c6e4c0a3d7bf.jpg_r_640x214_5f7b77f9.jpg',
          title: '东方盐湖城',
          desc: '华东地区最奇幻，最浪漫的道天下',
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1508/2d/a1f3f4042273bf.jpg_r_640x214_16a5afae.jpg',
          title: '觅龙城的故事',
          desc: '两千多年历史的常州，道不尽悠悠历史',
        },
        {
          id: '0004',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1811/58/a02ad3ab47e3e3.jpg_r_640x214_08977098.jpg',
          title: '扬州大明寺',
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
.item-img-wraper
  overflow hidden
  height 0
  padding-bottom 33.9%
  .item-img
    width 100%
.item-info
  padding .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>
