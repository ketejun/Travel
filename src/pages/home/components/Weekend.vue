<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fb/302620ed8350f8.jpg_r_640x214_25a07cb4.jpg',
          title: '橘子洲',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/88/8d3b492ebf0b16.jpg_r_640x214_7b3a281d.jpg',
          title: '橘子洲湘江游艇',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/b4/71c01c98139cf.jpg_r_640x214_30bac495.jpg',
          title: '靖港古镇',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1507/95/bf81a1519705f0.jpg_r_640x214_b29fb0c8.jpg',
          title: '长沙世界之窗',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/89/b2beff9f28b0db.jpg_r_640x214_94143396.jpg',
          title: '长沙生态动物园',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: 0.2rem
    line-height: 0.4rem
    background: #eee
    text-indent: 0.2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.2%
    .item-img
      width: 100%
  .item-info
    padding: 0.1rem
  .item-title
    line-height: 0.54rem
    font-size: 0.32rem
    ellipsis()
  .item-desc
    line-height: 0.4rem
    color: #ccc
    ellipsis()
</style>
