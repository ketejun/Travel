<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/57/579b6c97900745db.water.jpg_200x200_f09770c8.jpg',
          title: '橘子洲',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1610/8f/8f244e6a0ac12325a3.img.jpg_200x200_a6a1cd22.jpg',
          title: '橘子洲湘江游艇',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1412/68/42da26a54c27a3c237b4d10a61583c36.water.jpg_200x200_a38c904d.jpg',
          title: '靖港古镇',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1905/29/296e5659470d69bea3.img.jpg_200x200_75593f9f.jpg',
          title: '长沙世界之窗',
          desc: '湘江北去，橘子洲头，指点江山，激扬文字，问苍茫大地谁主沉浮'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b7aa220089fa8054e6e012bafff63042.jpg_200x200_650160bf.jpg',
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
  .recommend-title
    margin-top: 0.2rem
    line-height: .4rem
    background: #eee
    text-indent: 0.2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: 0.1rem
    .item-info
      flex: 1
      padding: 0.1rem
      min-width: 0
      .item-title
        line-height: 0.54rem
        font-size: 0.32rem
        ellipsis()
      .item-desc
        line-height: 0.4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: 0.44rem
        margin-top: 0.2rem
        background: #ff9300
        padding: 0 0.1rem
        border-radius: 0.06rem
        color: #fff
</style>
